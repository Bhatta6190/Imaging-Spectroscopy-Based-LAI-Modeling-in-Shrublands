# LAI Estimation from UAS MSI and AVIRIS-NG Imaging Spectroscopy

This repository contains the main analysis notebooks, processed ground LAI data, fire-boundary shapefiles, and predicted LAI raster outputs associated with the manuscript on scaling leaf area index (LAI) estimation from UAS multispectral imagery to airborne AVIRIS-NG imaging spectroscopy in fire-driven fynbos shrublands.

The repository is intended to support transparency and reproducibility for the analyses reported in the paper. All processing steps for the ground LAI measurements and remote sensing datasets are described in detail in the manuscript.

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

Contains predicted LAI raster outputs generated from AVIRIS-NG-based models. These rasters represent landscape-scale LAI predictions derived from the modeling workflow described in the manuscript.

### `Fire_boundaries_shapes/`

Contains fire-boundary shapefiles used to define and visualize the post-burn chronosequence study areas.

### `ground_LAI_data_processed/`

Contains processed ground LAI data used for model calibration and evaluation. The original field-measurement workflow and processing approach are described in the manuscript.

### `Airborne_MSI_analysis.ipynb`

Notebook for airborne MSI-equivalent analysis. This includes analysis of AVIRIS-NG data resampled to multispectral bands comparable to the UAS MSI bands, along with raw and harmonized modeling workflows.

### `HSI_band_ratio_optimization.ipynb`

Notebook for full-spectrum AVIRIS-NG hyperspectral index and band-ratio analysis, including optimization of spectral predictors for LAI estimation.

### `uas_and_AVIRIS_NG_modeling_analysis.ipynb`

Main notebook for UAS MSI and AVIRIS-NG modeling analysis, including vegetation-index calculation, model fitting, cross-validation, and comparison across sensor configurations.

## Data and Processing Notes

This repository contains processed data and analysis products required to reproduce the main modeling results. Large raw remote sensing datasets, original UAS image collections, and full AVIRIS-NG flightline products are not included.

The manuscript explains the full processing workflow, including:

- ground LAI data collection and processing;
- UAS multispectral image processing and plot-level spectral extraction;
- AVIRIS-NG reflectance data preparation;
- resampling of AVIRIS-NG data to MSI-equivalent bands;
- UAS-guided harmonization of airborne predictors;
- vegetation-index and custom spectral-index calculation;
- LAI model fitting, leave-one-out cross-validation, and raster prediction.

## Software

The analysis notebooks were developed in Python. Common scientific Python libraries used in the workflow include:

- `numpy`
- `pandas`
- `geopandas`
- `rasterio`
- `scikit-learn`
- `matplotlib`
- `seaborn`

Additional package requirements may depend on the local geospatial Python environment used to run the notebooks.

## Recommended Use

To reproduce the analysis, run the notebooks in the following general order:

1. `uas_and_AVIRIS_NG_modeling_analysis.ipynb`
2. `Airborne_MSI_analysis.ipynb`
3. `HSI_band_ratio_optimization.ipynb`

Users should refer to the manuscript for detailed methodological context, including data preprocessing, predictor definitions, model forms, validation strategy, and interpretation of the LAI products.

## Citation

If you use this repository, please cite the associated manuscript:

> Bhatta, R., Chancia, R., Chaity, M. D., Lekhak, S., Slingsby, J., and van Aardt, J. Manuscript in preparation.

The citation should be updated with the final journal reference once the paper is published.

## License

This repository is distributed under the license provided in the `LICENSE` file.
