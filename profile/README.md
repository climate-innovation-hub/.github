This GitHub Organisation contains code and information relating to the CSIRO Climate Innovation Hub.

## Respositories

The following is a summary of the repositories in this GitHub Organisation:

| Repo | Description | Status | Catalogue |
| ---  | ---         | ---    | ---       |
| [agcd-csiro](https://github.com/AusClimateService/agcd-csiro) | Scripts for creating a replica of CSIRO's commercially licensed version of the AGCD dataset on NCI | Active | |
| [agcd-masking](https://github.com/climate-innovation-hub/agcd-masking) | Code for applying AGCD data quality masks (and generic shapefile masks) | Active | |
| [attribute-editing](https://github.com/climate-innovation-hub/attribute-editing) | Code for applying CIH metadata to netCDF file attributes | Active | |
| [CRE_Indices](https://github.com/climate-innovation-hub/CRE_Indices) | Code for calculating agriculture metrics | Archived | |
| [fed-uni](https://github.com/climate-innovation-hub/fed-uni) | Code used to pre-process data from July 2022 partnership with Federation University | Archived | |
| [frequency-analysis](https://github.com/climate-innovation-hub/frequency-analysis) | Code for frequency analysis (e.g. return period calculation) | Active | | 
| [indices](https://github.com/AusClimateService/indices) | Code for calculating climate indices (hosted in the ACS GitHub Organisation) | Active | CIHP-2 |
| [qqscale](https://github.com/climate-innovation-hub/qqscale) | Code for quantile-quantile scaling | Active | |
| [shapefiles](https://github.com/aus-ref-clim-data-nci/shapefiles) | Collection of shapefiles commonly used by the Australian climate research community | Active | |
| [workflows](https://github.com/climate-innovation-hub/workflows) | Workflows (e.g. notebooks) used to create application-ready data | Archived | CIHP-1:[`qq_scale/`](https://github.com/climate-innovation-hub/workflows/tree/master/qq_scale)<br/>CIHP-3:[`ffdi/`](https://github.com/climate-innovation-hub/workflows/tree/master/ffdi) |
 

## wp00

Our project space on NCI is organised as follows:

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

Individual users have write access to their own directories in `users/`.

Only people in the writers group `wp00_w` have write access to the `data/`, `projects/` and `shared-code/` directories.

Detailed data reference syntax for some of the directories listed above can be found at these links:
- [`wp00/data/QQ-CMIP6/`](https://github.com/climate-innovation-hub/.github-private/blob/main/drs-qq-cmip6.md)
