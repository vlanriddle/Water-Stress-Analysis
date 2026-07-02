Water Stress Analysis in India using GeoPandas

Overview

This project performs a GIS-based water stress assessment across Indian districts using Python and GeoPandas. Multiple geospatial and demographic datasets are integrated to estimate a **Water Stress Index** based on water availability and water demand indicators.

The project demonstrates geospatial data processing, spatial analysis, raster-vector integration, and thematic map visualization.
 
Objectives
Analyze spatial variation in water stress across Indian districts.
Integrate multiple geospatial datasets into a unified GIS workflow.
Visualize water stress using choropleth maps.
Export processed geospatial data for further analysis.

 Datasets Used

| Dataset | Source | Purpose |
|---------|--------|---------|
| India District Boundaries (GADM Level-2) | https://gadm.org | Administrative boundaries for district-level analysis |
| HydroRIVERS v1.0 | https://www.hydrosheds.org/products/hydrorivers | River network across India |
| HydroLAKES v1.0 | https://www.hydrosheds.org/products/hydrolakes | Lake polygons |
| WorldClim Version 2.1 Monthly Precipitation | https://www.worldclim.org/data/monthlywth.html | Monthly rainfall raster |
| India Census District Demographics | https://www.dataful.in | District-wise population and demographic statistics |

Technologies Used
Python
 GeoPandas
 Pandas
 Rasterio
 Rasterstats
 NumPy
 Matplotlib

Project Workflow

1. Data Collection

Downloaded and organized:

Administrative boundaries
River network
Lake polygons
Rainfall raster
Population dataset

2. Data Preprocessing

Loaded vector datasets using GeoPandas
Loaded rainfall raster using Rasterio
Converted all layers into a common CRS
Cleaned and merged population data with district boundaries
Calculated district area (km²)

3. Spatial Analysis

Performed the following analyses:

Population Density
Mean Rainfall (Zonal Statistics)
River Count per District
Lake Count per District

 4. Feature Engineering

Normalized all variables using Min-Max Scaling.

Variables used:

Rainfall
Population Density
River Count
Lake Count

5. Water Stress Index

The Water Stress Index was calculated using a weighted approach:
Water Stress =
0.40 × (Low Rainfall)
+ 0.30 × Population Density
+ 0.20 × River Availability
+ 0.10 × Lake Availability

The resulting index was classified into:

Very Low
Low
Moderate
High
Very High

 Outputs

Maps

Population Density Map
Rainfall Distribution Map
Water Stress Index Map

Sample Visualization

The final output is a district-level choropleth map showing the spatial distribution of water stress across India.

Disclaimer

This project presents a **GIS-based Water Stress Index** for educational and analytical purposes. It is not an official measure of water stress. The index is derived from selected spatial indicators and is intended to demonstrate geospatial analysis techniques using open-source datasets.
