This GitHub Organisation contains code and information relating to the CSIRO Climate Innovation Hub.

Many of the repositories linked below are private and only visible to members of the Climate Innovation Hub GitHub Organisation.

## Active Respositories

The following is a summary of the repositories in this GitHub Organisation that are in active use/development.

| Repo | Description | 
| ---  | ---         | 
| [agcd-csiro](https://github.com/AusClimateService/agcd-csiro) | Scripts for creating a replica of CSIRO's commercially licensed version of the AGCD dataset on NCI |
| [agcd-masking](https://github.com/climate-innovation-hub/agcd-masking) | Code for applying AGCD data quality masks (and generic shapefile masks) |
| [attribute-editing](https://github.com/climate-innovation-hub/attribute-editing) | Code for applying CIH metadata to netCDF file attributes |
| [cih-utils](https://github.com/climate-innovation-hub/cih-utils) | General utility code used in the CIH |
| [frequency-analysis](https://github.com/climate-innovation-hub/frequency-analysis) | Code for frequency analysis (e.g. return period calculation) | 
| [ivcap-sdk](https://github.com/climate-innovation-hub/ivcap_sdk) | Development library to interact with the Climate Intelligence Platform |

The [indices](https://github.com/AusClimateService/indices) and [qqscale](https://github.com/AusClimateService/qqscale) repositories hosted by the Australian Climate Service
and [shapefiles](https://github.com/aus-ref-clim-data-nci/shapefiles) repository hosted by the Australian Community Reference Climate Data Collection
are also used and contributed to by CIH staff.

## Product repositories

The following is a summary of the repositories corresponding to particular CIH products.

| Product | Repo |
| ---  | ---         |
| CIHP-1 | [cihp-1-application-ready-climate-projections](https://github.com/climate-innovation-hub/cihp-1-application-ready-climate-projections) |
| CIHP-2 | [cihp-2-climate-diagnostics](https://github.com/climate-innovation-hub/cihp-2-climate-diagnostics) |
| CIHP-3 | [cihp-3-forest-fire-danger-index](https://github.com/climate-innovation-hub/cihp-3-forest-fire-danger-index) |
| CIHP-4 | [cihp-4-seasonal-rainfall](https://github.com/climate-innovation-hub/cihp-4-seasonal-rainfall) |
| CIHP-4-1 | [cihp-4-1-growing-season-rainfall](https://github.com/climate-innovation-hub/cihp-4-1-growing-season-rainfall) |
| CIHP-4-2 | [cihp-4-2-summer-fallow-rainfall](https://github.com/climate-innovation-hub/cihp-4-2-summer-fallow-rainfall) | 
| CIHP-4-3 | [cihp-4-3-late-season-frost-risk](https://github.com/climate-innovation-hub/cihp-4-3-late-season-frost-risk) |
| CIHP-4-4 | [cihp-4-4-late-season-heat-risk](https://github.com/climate-innovation-hub/cihp-4-4-late-season-heat-risk) |
| CIHP-4-5 | [cihp-4-5-heat-risk-at-joining](https://github.com/climate-innovation-hub/cihp-4-5-heat-risk-at-joining) |
| CIHP-5 | [cihp-5-coastal-inundation](https://github.com/climate-innovation-hub/cihp-5-coastal-inundation) |

The data processed in CIHP-1, CIHP-2, CIHP-3 and CIHP-4 (see the corresponding repositories for the processing code)
was the CMIP5 quantile delta change projections data produced using the code in the 
[`qq_scale/`](https://github.com/climate-innovation-hub/workflows/tree/master/qq_scale) directory
of the workflows repo.

A complete history of the code used for quantile delta change projections at CSIRO can be found
[here](https://github.com/climate-innovation-hub/qq-history).

## Archived Respositories

The following is a summary of the repositories in this GitHub Organisation that no longer in use and/or
have been archived for the purposes of data provenance.

| Repo | Description |
| ---  | ---         |
| [CRE_Indices](https://github.com/climate-innovation-hub/CRE_Indices) | Code for calculating agriculture metrics |
| [fed-uni](https://github.com/climate-innovation-hub/fed-uni) | Code used to pre-process data from July 2022 partnership with Federation University |
| [workflows](https://github.com/climate-innovation-hub/workflows) | Workflows (e.g. notebooks) used to create application-ready data | 

## wp00

Our project space on NCI is organised as follows:

```
wp00/
├── data/
│   ├── CIHP4/
│   ├── CIHP5/
│   ├── observations/
│   ├── QQ-CMIP5/
│   └── QDC-CMIP6/
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
