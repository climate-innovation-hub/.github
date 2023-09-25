This GitHub Organisation contains code and information relating to the CSIRO Climate Innovation Hub.

## Active Respositories

The following is a summary of the repositories in this GitHub Organisation that are in active use/development.

| Repo | Description | 
| ---  | ---         | 
| [agcd-csiro](https://github.com/AusClimateService/agcd-csiro) | Scripts for creating a replica of CSIRO's commercially licensed version of the AGCD dataset on NCI |
| [agcd-masking](https://github.com/climate-innovation-hub/agcd-masking) | Code for applying AGCD data quality masks (and generic shapefile masks) |
| [attribute-editing](https://github.com/climate-innovation-hub/attribute-editing) | Code for applying CIH metadata to netCDF file attributes |
| [frequency-analysis](https://github.com/climate-innovation-hub/frequency-analysis) | Code for frequency analysis (e.g. return period calculation) | 
| [ivcap-sdk](https://github.com/climate-innovation-hub/ivcap_sdk) | Development library to interact with the Climate Intelligence Platform |
| [qqscale](https://github.com/climate-innovation-hub/qqscale) | Code for quantile-quantile scaling |

The [indices](https://github.com/AusClimateService/indices) repository hosted by the Australian Climate Service
and [shapefiles](https://github.com/aus-ref-clim-data-nci/shapefiles) repository hosted by the Australian Community Reference Climate Data Collection
are also used and contributed to by CIH staff.
 
## Archived Respositories

The following is a summary of the repositories in this GitHub Organisation that no longer in use and/or
have been archived for the purposes of data provenance.

| Repo | Description |
| ---  | ---         |
| [cihp-1-application-ready-climate-projections](https://github.com/climate-innovation-hub/cihp-1-application-ready-climate-projections) | Code for CIHP-1 products |
| [cihp-2-climate-diagnostics](https://github.com/climate-innovation-hub/cihp-2-climate-diagnostics) | Code for CIHP-2 products |
| [cihp-4-seasonal-rainfall](https://github.com/climate-innovation-hub/cihp-4-seasonal-rainfall) | Code for CIHP-4 products |
| [cihp-4-1-growing-season-rainfall](https://github.com/climate-innovation-hub/cihp-4-1-growing-season-rainfall) | Code for CIHP-4-1 |
| [cihp-4-2-summer-fallow-rainfall](https://github.com/climate-innovation-hub/cihp-4-2-summer-fallow-rainfall) | Code for CIHP-4-2 |
| [cihp-4-3-late-season-frost-risk](https://github.com/climate-innovation-hub/cihp-4-3-late-season-frost-risk) | Code for CIHP-4-3 |
| [cihp-4-5-heat-risk-at-joining](https://github.com/climate-innovation-hub/cihp-4-5-heat-risk-at-joining) | Code for CIHP-4-5 |
| [CRE_Indices](https://github.com/climate-innovation-hub/CRE_Indices) | Code for calculating agriculture metrics |
| [fed-uni](https://github.com/climate-innovation-hub/fed-uni) | Code used to pre-process data from July 2022 partnership with Federation University |
| [workflows](https://github.com/climate-innovation-hub/workflows) | Workflows (e.g. notebooks) used to create application-ready data | 

The data processed in CIHP-1, CIHP-2 and CIHP-4 (see the corresponding repositories for the processing code)
was the CMIP5 quantile delta mapped projections data produced using the code in the 
[`qq_scale/`](https://github.com/climate-innovation-hub/workflows/tree/master/qq_scale) directory
of the workflows repo.

A complete history of the code used for quantile delta mapping at CSIRO can be found
[here](https://github.com/climate-innovation-hub/.github-private/blob/main/qq-history.md).

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
