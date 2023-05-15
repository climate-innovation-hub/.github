## Data Reference Syntax: CMIP6 application ready data

The Climate Innovation Hub produces CMIP6 application ready climate projection data
using the quantile delta change method described in the
[qqscale repository](https://github.com/climate-innovation-hub/qqscale). 

The directories associated with those data follow this structure:
```
/g/data/wp00/data/QQ-CMIP6/{method}/{model}/{experiment}/{run}/{timescale}/{variable}/{version}/
```
For example:
```
/g/data/wp00/data/QQ-CMIP6/qdc/ACCESS-ESM1-5/ssp370/r1i1p1f1/day/tasmin/v20191115/
```

The various methods include:
- `qdc`: quantile delta change
- `mdc`: mean delta change
- `qmba`: quantile mapping bias adjustment
- `ssr`: singularity stochastic removal

Each directory contains the application ready data
and may also contain related files such as
the adjustment factors calculated during the quantile delta change process
and a jupyter notebook containing visualisations of the data (i.e. for sanity checking).

The application ready data files follow this structure:
```
{variable}_{timescale}_{model}_{experiment}_{run}_{domain}-{grid}_{start-time}_{end-time}_{qq-methods}_{target-dataset}-{target-start}-{target-end}_historical-{hist-start}-{hist-end}_{matching}.nc
```

For example:
```
pr-ssr_day_ACCESS-ESM1-5_ssp370_r1i1p1f1_AUS-r005_20350101-20641231_qdc-multiplicative-monthly-linear-q100_AGCD-19900101-20191231_historical-19950101-20141231_monthly-mean-match.nc
```

Fields that need more explanation are included in the table below.

| Field | Definition / options |
| ---   | ---                  |
| `{variable}` | If SSR was used in the quantile delta change calculation this field ends with `-ssr`. |
| `{qq-methods}` | Contains five sub-fields `{method}-{scaling}-{timescale}-{interpolation}-{quantiles}` where the scaling can be `additive` or `multiplicative`; the timescale is that of the adjustment factors; interpolation to locate adjustment factors can be `nearest`, `linear` or `cubic`; and `quantiles` decribes the number of quantiles used (e.g. `q100`) | 
| `{target-dataset}` | The dataset that the quantile delta scaling was applied to (usually AGCD). |
| `{hist-start}-{hist-end}` | The historical time period used in calculating the adjustment factors. |
| `{matching}` | Included if a final adjustment was applied to match the model mean change to the qq-scaled mean change. Can be an annual mean (`annual-mean-match`) or monthly mean (`monthly-mean-match`) match. | 
