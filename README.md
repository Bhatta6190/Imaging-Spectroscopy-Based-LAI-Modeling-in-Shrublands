# UAS-Guided Harmonization of Airborne Imaging Spectroscopy for LAI Retrieval

This repository contains the main analysis notebooks, processed ground LAI data, fire-boundary shapefiles, and predicted LAI raster outputs associated with the manuscript:

**UAS-Guided Harmonization of Airborne Imaging Spectroscopy for Scaling Leaf Area Index Retrieval in Fire-Driven Mediterranean Shrublands**

The study evaluates how field-measured leaf area index (LAI), UAS multispectral imagery, and airborne AVIRIS-NG imaging spectroscopy can be linked to estimate and scale LAI across structurally complex fynbos shrublands at Grootbos Private Nature Reserve, South Africa.

The repository is intended to support transparency and reproducibility for the analyses reported in the paper. All processing steps for the ground LAI measurements and remote sensing datasets are described in detail in the manuscript.

## Study Overview

LAI retrieval is challenging in low-stature, fire-driven shrublands because open canopies, exposed soil, senescent material, woody structure, shadow, and fine-scale vegetation heterogeneity weaken conventional greenness-based spectral relationships. This work treats high-resolution UAS multispectral observations as an intermediate scaling layer between plot-level field measurements and airborne imaging spectroscopy.

The analysis focuses on:

- field LAI measurements from CI-110 hemispherical canopy imagery;
- UAS multispectral imagery acquired with a DJI Mavic 3 Multispectral sensor;
- AVIRIS-NG Level-2B surface reflectance from the NASA BioSCape campaign;
- airborne MSI-equivalent analysis using AVIRIS-NG data resampled to UAS-like bands;
- UAS-guided harmonization of airborne spectral predictors;
- full-spectrum AVIRIS-NG index and band-ratio analysis;
- LAI model fitting, leave-one-out cross-validation, and landscape-scale LAI prediction.

## Repository Contents

```text
.
├── AVIRIS_Predicted_LAI_Rasters/
├── Fire_boundaries_shapes/
├── ground_LAI_data_processed/
├── Airborne_MSI_analysis.ipynb
├── HSI_band_ratio_optimization.ipynb
├── uas_and_AVIRIS_NG_modeling_analysis.ipynb
├── LICENSE
└── README.md
```

## Folder and File Descriptions

### `AVIRIS_Predicted_LAI_Rasters/`

Contains predicted LAI raster outputs generated from AVIRIS-NG-based models. These rasters represent landscape-scale LAI predictions derived from the harmonized airborne imaging spectroscopy workflow described in the manuscript.

### `Fire_boundaries_shapes/`

Contains fire-boundary shapefiles used to define and visualize the post-burn chronosequence study areas at Grootbos Private Nature Reserve.

### `ground_LAI_data_processed/`

Contains processed ground LAI data used for model calibration and evaluation. These data are derived from CI-110 Plant Canopy Analyzer hemispherical imagery and gap-fraction processing. The field-measurement workflow, image thresholding, zenith-angle restriction, and plot-level LAI processing are described in the manuscript.

### `Airborne_MSI_analysis.ipynb`

Notebook for airborne MSI-equivalent analysis. This includes analysis of AVIRIS-NG reflectance data resampled to multispectral bands comparable to the UAS MSI bands, along with raw and UAS-guided harmonized modeling workflows.

### `HSI_band_ratio_optimization.ipynb`

Notebook for full-spectrum AVIRIS-NG hyperspectral index and band-ratio analysis, including optimized wavelength-pair predictors and SWIR-sensitive indices for LAI estimation.

### `uas_and_AVIRIS_NG_modeling_analysis.ipynb`

Main notebook for UAS MSI and AVIRIS-NG modeling analysis, including vegetation-index calculation, model fitting, leave-one-out cross-validation, cross-sensor comparison, and harmonized LAI prediction.

## Data and Processing Notes

This repository contains processed data and analysis products required to reproduce the main modeling results. Large raw remote sensing datasets, original UAS image collections, and full AVIRIS-NG flightline products are not included.

Raw CI-110 ground measurement files are included in the directory `Raw_CI_110_LAI_data`. The `ground_LAI_data_processed/` folder contains processed LAI data within the spatial shapefile used in the manuscript analyses.

The manuscript explains the full processing workflow, including:

- ground LAI data collection and CI-110 image processing;
- UAS multispectral image processing and plot-level spectral extraction;
- AVIRIS-NG Level-2B reflectance data preparation;
- resampling of AVIRIS-NG data to MSI-equivalent bands;
- UAS-guided harmonization of airborne predictors;
- vegetation-index and custom spectral-index calculation;
- LAI model fitting, leave-one-out cross-validation, and raster-based LAI prediction.

## Software

The analysis notebooks were developed in Python. Common scientific Python libraries used in the workflow include:

- `numpy`
- `pandas`
- `geopandas`
- `rasterio`
- `scikit-learn`
- `matplotlib`
- `seaborn`

Additional package requirements may depend on the local geospatial Python environment used to run the notebooks. Kindly, refer to the notebooks for all needed packages.

## Recommended Use

To reproduce the analysis, run the notebooks in the following general order:

1. `HSI_band_ratio_optimization.ipynb`
2. `uas_and_AVIRIS_NG_modeling_analysis.ipynb`
3. `Airborne_MSI_analysis.ipynb`

Users should refer to the manuscript for detailed methodological context, including data preprocessing, predictor definitions, model forms, validation strategy, and interpretation of the LAI products.

## Citation

If you use this repository, please cite the associated manuscript:

> Bhatta, R., Chancia, R., Chaity, M. D., Lekhak, S., Slingsby, J., and van Aardt, J. UAS-Guided Harmonization of Airborne Imaging Spectroscopy for Scaling Leaf Area Index Retrieval in Fire-Driven Mediterranean Shrublands. Manuscript in preparation.

The citation should be updated with the final journal reference once the paper is published.

## Author Information

| Author |
|---|
| [Ramesh Bhatta](https://scholar.google.com/citations?user=O7m5LxEAAAAJ&hl=en) |
| [Manisha Das Chaity](https://scholar.google.com/citations?user=kaMzs9YAAAAJ&hl=en) |
| [Sagar Lekhak](https://scholar.google.com/citations?user=Mkf-WgsAAAAJ&hl=en) |
| [Jasper Slingsby](https://scholar.google.com/citations?user=ZjBauSkAAAAJ&hl=en) |
| [Jan van Aardt](https://scholar.google.com/citations?user=GdWlA6gAAAAJ&hl=en) |


## AI Assistance Note

This README file was prepared with assistance from ChatGPT and was reviewed and verified by the author, Ramesh Bhatta. If any discrepancy or unclear information is identified and reported,the author would be happy to review and resolve it.

## License

This repository is distributed under the license provided in the `LICENSE` file.
