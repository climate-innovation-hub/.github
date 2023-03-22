This GitHub Organisation contains code and information relating to the CSIRO Climate Innovation Hub.

## Respositories

The following is a summary of the repositories in this GitHub Organisation:

#### Code/software currently in use

- [agcd-masking](https://github.com/climate-innovation-hub/agcd-masking): Code for masking AGCD data
- [attribute-editing](https://github.com/climate-innovation-hub/attribute-editing): Code for editing netCDF file attributes
- [frequency-analysis](https://github.com/climate-innovation-hub/frequency-analysis): Code for frequency analysis (e.g. return period calculation)
- [indices](https://github.com/AusClimateService/indices): Code for calculating climate indices (hosted in the ACS GitHub Organisation)
- [qqscale](https://github.com/climate-innovation-hub/qqscale): Code for quantile-quantile scaling
- [shapefiles](https://github.com/aus-ref-clim-data-nci/shapefiles): Collection of shapefiles commonly used by the Australian climate research community (hosted by the Australian Community Reference Climate Data Collection)

#### Code/software used in the past but not currently in use

- [fed-uni](https://github.com/climate-innovation-hub/fed-uni): Code used to process data from July 2022 partnership with Federation University
- [workflows](https://github.com/climate-innovation-hub/workflows): Workflows (e.g. notebooks) used to create application-ready data
- [CRE_Indices](https://github.com/climate-innovation-hub/CRE_Indices): Code for calculating agriculture metrics


## wp00

Our project space on NCI should ideally be organised as follows:

```
wp00/
├── data/
│   ├── QQ-CMIP5/
│   └── QQ-CMIP6/
├── projects/
│   └── fed-uni/
├── shared-code/
│   ├── agcd-masking/
│   ├── attribute-editing/
│   ├── frequency-analysis/
│   └── qqscale/
├── users/
│   ├── ajt547/
│   ├── ct5255/
│   ├── dbi599/
│   ├── gd7113/
│   ├── kcn599/
│   ├── pjt554/
│   ├── rb4844/
│   ├── rg9861/
│   └── rxd603/
```

Individual users will have write access to their own directories in `users/`.
Only people in the writers group `wp00_w` will have write access to the `data/`, `projects/` and `shared-code/` directories.
