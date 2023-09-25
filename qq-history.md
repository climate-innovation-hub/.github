## Quantile Delta Mapping at CSIRO

For many years now,
CSIRO has produced climate projection data by applying modelled quantile delta changes
(e.g. between an historical and future model simulation)
either additively or multiplicatively to observational data.
This method is often referred to a "quantile-quantile scaling" around CSIRO,
but in the literature has been labelled "Quantile Delta Mapping"
(QDM; [Cannon et al 2015](https://doi.org/10.1175/JCLI-D-14-00754.1)).

The software/code used to apply the QDM method has evolved over the years.

### Old code
 
1. Kim Nguyen and Craig Heady developed an original version of the code for the NRM project.
   It implemented a decile scaling approach with individual percentiles included for the top 90th up and bottom less than 10th percentiles.
   This was used to create the application ready rainfall data that is available through Climate Change in Australia.
   It used a combination of shell scripting, ferret, cdo and fortran code.
   Overall it worked well, but the authors identified some things where the performance wasn’t quite as good as they'd hoped for (e.g. seasonal average change).
   The code for this original version isn't inlcuded in the CIH GitHub Organisation.

2. Marcus Thatcher and Craig developed a completely new fortran code version for the VCP19 (DELWP) project work (see `fortran/`).
   This had some subtle changes in the approach to see their “hunch” about why it behaved in a certain way could be improved.
   It added completely individual percentile binning (100 of them)
   with interpolation for change values depending on where the individual daily values fell in-between percentile bins.
   This improved the average seasonal change performance as predicted.

3. The Climate Innovation Hub came into being and Raktima Dey and Vassili Kitsios started writing a python version,
   which can be found at the [workflows](https://github.com/climate-innovation-hub/workflows/tree/master/qq_scale) repo.
   It implements the same improved method as the previous fortran method that Marcus and Craig developed
   and was used to produce CMIP5-based projections data for early CIH clients. 

These methods are documented on the [CCiA website](https://www.climatechangeinaustralia.gov.au/en/obtain-data/application-ready-data/scaling-methods/)
and also in a [CAWCR Technical Report](http://www.bom.gov.au/research/publications/cawcrreports/CTR_034.pdf).

A Climate Innovation Hub technical report describes the methodology used in the Python version as follows:

> Firstly, for each of the model simulated baseline and future periods,
> for each month of the year,
> all daily data are ranked from highest to lowest,
> and then divided equally into 100 bins or “quantiles”.
> The first quantile contains the first 1% of data values,
> the second quantile contains the next 1% of data values and so forth.
> A change factor is then calculated as the difference between the mean of the historical and future data for each quantile. 
>
> Then, the equivalent quantiles are calculated using relevant observed (AGCD v1 or ERA5) data
> (for each month under consideration) over the historical baseline period,
> and each daily value is assigned to a quantile.
> Then, the change factor for a given quantile is applied to the corresponding observed daily value
> for that quantile to produce a future daily value.
> For example, if the change factor for the 70th quantile of daily precipitation is +10%,
> and the observed daily precipitation value for the 70th quantile is 50mm,
> then the future daily value becomes 55mm.
> Since change factors can vary between month,
> the seasonal variability in simulated future climate changes is incorporated into the QQ-scaled data. 
>
> Finally, some adjustments are applied to the QQ-scaled data
> to ensure consistency with the GCM-simulated changes in average climate conditions
> and to ensure that values are physically plausible.
> Firstly, the QQ scaled data are adjusted so that the change in monthly mean
> between observations and QQ-scaled data matches the model simulated change in monthly mean.
> For example, if QQ scaling produces a mean change of +15% for a given month,
> but the climate model simulates a mean change of +18%,
> then all daily values are adjusted upward by an extra 3%.
> Finally, for solar radiation and relative humidity a ‘cap’ or upper limit to the data
> is introduced at this stage to ensure that solar radiation does not exceed the maximum possible
> (i.e., clear-sky solar radiation) and that relative humidity does not exceed 100%. 

The only thing this description doesn't mention is the interpolation of change values
depending on where the individual daily values fell in-between percentile bins.

### Current code

In an effort to improve the performance of the qq-scaling code used by the CIH,
Damien Irving has used the bias adjustment and downscaling functionality in the
[xclim]((https://xclim.readthedocs.io)) package to implement the QDM method.

The code Damien has developed is being used to produce CMIP6-based projections data for the CIH
and also bias corrected CORDEX data for the Australian Climate Service.

https://github.com/climate-innovation-hub/qqscale