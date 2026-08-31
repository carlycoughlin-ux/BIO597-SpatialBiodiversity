# Schedule


| Week | Topic | Main Python Tools | Exercises |
| --- | --- | --- | --- |
| [Week 1 (09/04)](week-01.md) | Spatial thinking in biodiversity science | NumPy, pandas, GeoPandas, matplotlib | Map a biodiversity dataset |
| [Week 2 (09/11)](week-02.md) | Coordinate systems and spatial geometry | GeoPandas, pyproj, Shapely | Reproject data and measure distances |
| [Week 3 (09/18)](week-03.md) | Vector spatial analysis | GeoPandas, Shapely | Buffers, intersections, spatial joins |
| [Week 4 (09/25)](week-04.md) | Biodiversity data acquisition and cleaning | pandas, GeoPandas, pygbif, requests | Download and clean GBIF observations |
| [Week 5 (10/02)](week-05.md) | Raster data and environmental covariates | rasterio, rioxarray, xarray, NumPy | Extract climate, elevation, and land cover |
| [Week 6 (10/09)](week-06.md) | Spatial sampling and sampling bias | NumPy, GeoPandas, scikit-learn, scipy | Compare raw, thinned, and stratified samples |
| [Week 7 (10/16)](week-07.md) | Measuring spatial biodiversity patterns | pandas, NumPy, GeoPandas, scipy | Map richness, diversity, endemism, and rarity |
| [Week 8 (10/23)](week-08.md) | Spatial autocorrelation | libpysal, esda, GeoPandas | Calculate global and local Moran's I |
| [Week 9 (10/30)](week-09.md) | Species distribution modeling | scikit-learn, rasterio, pandas | Build and compare distribution models |
| [Week 10 (11/06)](week-10.md) | Spatial interpolation and prediction | scipy, scikit-learn, optionally gstools | Predict an environmental or ecological surface |
| [Week 11 (11/13)](week-11.md) | Community composition across space | pandas, scipy, scikit-learn, GeoPandas | Analyze beta diversity and distance decay |
| [Week 12 (11/20)](week-12.md) | Ordination, gradients, and evolutionary diversity | scikit-learn, scipy, matplotlib | Compare geographic, environmental, and diversity spaces |
| [Week 13 (12/04)](week-13.md) | Landscape connectivity and conservation prioritization | rasterio, NumPy, networkx | Build resistance and prioritization scenarios |
| [Week 14 (12/11)](week-14.md) | Spatial machine learning and model evaluation | scikit-learn, GeoPandas, NumPy | Compare random and spatial cross-validation |
| [Week 15 (12/18)](week-15.md) | Synthesis: biodiversity under environmental change | Full stack | Final project presentations |

Each week page provides a template for learning goals, readings, lab activities, and deliverables.

## Weekly Topic Outline

### Week 1: Spatial Thinking in Biodiversity Science

Students begin with why geography matters in ecology and evolution. They make basic maps, species-specific maps, sampling-density maps, histograms, and a species-by-site matrix from a simple biodiversity dataset.

### Week 2: Coordinate Systems and Spatial Geometry

The course introduces latitude and longitude, projected coordinate systems, datums, EPSG codes, geometry operations, and the ecological consequences of measuring distances in the wrong coordinate system.

### Week 3: Vector Spatial Analysis

Students use spatial joins, buffers, intersections, nearest-neighbor operations, point-in-polygon tests, and distance matrices to answer practical spatial ecology questions.

### Week 4: Biodiversity Data Acquisition and Cleaning

Students download occurrence data, handle taxonomic and coordinate uncertainty, remove duplicates, flag impossible coordinates, and document metadata and cleaning decisions.

### Week 5: Raster Data and Environmental Covariates

Students learn raster concepts including cells, pixels, resolution, extent, NoData, alignment, elevation, climate, land cover, remote sensing, and microclimate. They extract environmental values at occurrence locations.

### Week 6: Spatial Sampling and Sampling Bias

Students compare random, stratified, clustered, thinned, and biased samples to see how sampling design affects richness estimates, rare species detection, and downstream models.

### Week 7: Measuring Spatial Biodiversity Patterns

The course moves from GIS operations to biodiversity metrics: richness, Shannon diversity, Simpson diversity, endemism, rarity, alpha/beta/gamma diversity, moving-window diversity, and spatial aggregation.

### Week 8: Spatial Autocorrelation

Students calculate global and local spatial autocorrelation and ask when nearby observations are more similar than expected by chance.

### Week 9: Species Distribution Modeling

Students model species-environment relationships using presence/absence, presence/background, pseudoabsence, logistic regression, and random forests, then compare spatial predictions.

### Week 10: Spatial Interpolation and Prediction

Students distinguish interpolation from extrapolation, explore nearest-neighbor prediction, inverse distance weighting, kriging concepts, Gaussian processes, and prediction uncertainty.

### Week 11: Community Composition Across Space

The focus shifts from single-species analysis to multispecies communities using site-by-species matrices, Bray-Curtis and Jaccard dissimilarity, turnover, nestedness, and distance-decay relationships.

### Week 12: Ordination, Gradients, and Evolutionary Diversity

Students compare geographic space and environmental space using ordination, then connect community patterns to phylogenetic and functional diversity, trait data, missing data, and evolutionary history.

### Week 13: Landscape Connectivity and Conservation Prioritization

Students build resistance surfaces and graph representations of landscapes, then connect connectivity results to protected areas, complementarity, irreplaceability, and conservation prioritization.

### Week 14: Spatial Machine Learning and Model Evaluation

Students confront spatial leakage by comparing random train/test splits with spatial train/test splits. Topics include overfitting, spatial cross-validation, transferability, extrapolation, and model uncertainty.

### Week 15: Synthesis: Biodiversity Under Environmental Change

The final week pulls together biodiversity observations, spatial processing, environmental covariates, statistical and machine-learning models, spatial prediction, uncertainty, ecological interpretation, and final project presentations.
