# Software and Data

## Recommended Computing Environment

Choose either R or Python for the main workflow, but all analyses should be reproducible from scripts, notebooks, or a documented pipeline.

### R Packages

- `sf` for vector spatial data.
- `terra` or `stars` for raster data.
- `dplyr`, `tidyr`, and `ggplot2` for data wrangling and plotting.
- `targets` or `renv` for reproducibility.
- SDM and biodiversity packages selected as needed for course exercises.

### Python Packages

- `geopandas` for vector spatial data.
- `rasterio`, `rioxarray`, and `xarray` for raster data.
- `pandas`, `numpy`, and `scikit-learn` for data processing and modeling.
- `matplotlib`, `seaborn`, or `plotnine` for figures.
- `conda`, `mamba`, `uv`, or `venv` for environment management.

## Candidate Data Sources

- GBIF occurrence records.
- iNaturalist research-grade observations.
- VertNet or other taxon-specific occurrence repositories.
- WorldClim, CHELSA, PRISM, or ERA5 climate data.
- MODIS, Landsat, Sentinel, or derived remote sensing products.
- Soil, terrain, hydrology, land cover, and protected area datasets.
- OpenTree, VertLife, Fish Tree of Life, or clade-specific phylogenies.
- TRY, BIEN, GIFT, or other trait and range databases.

## Data Management Expectations

- Keep raw data separate from processed data.
- Record download dates, licenses, citations, and filtering decisions.
- Use relative paths inside project folders.
- Never manually edit raw data files without documenting the change.
