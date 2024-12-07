# Identifying Coastal Areas Best Suited for Potential Aquaculture Investment
![aquaculture-image](https://i0.wp.com/calmatters.org/wp-content/uploads/2020/05/NOAA_Mussellonglines_02.jpg?fit=1200%2C799&ssl=1)
Source : [Cal Matters](https://calmatters.org/environment/2020/05/california-shellfish-farming-aquaculture/)

This repository houses a function that generates a map of suitable habitats along the West Coast of the United States for potential aquaculture species. The calculation is based on the species of interest's suitable range of sea surface temperature (sst) and suitable range of depth below the sea level. The complete function is presented at the top of the document and the workflow for creating the function is explained in detail below. The function takes 5 arguments: 

- `species` str, the name of the species of interest
- `min_sst` int, the minimum sea surface temperature of the species
- `max_sst` int, the maximum sea surface temperature of the species
- `min_depth` int, the minimum depth of the species
- `max_depth` int, the maximum depth of the species

Information about a species' sst and depth range can be found at [Sea Life Base.](https://www.sealifebase.ca/search.php) 

## Skills
This analysis highlights

- Creating a function for raster zonal classification
- Working with vector data using `sf`
- Working with raster data using `terra`
- Working with economic data and remotely sensed sea surface temperature data and bathymetry data
- Raster resampling, reclassifying, and zonal algebra
- Mapmaking and data visualization using `tmap` 

## Description
File map
```
├── aquaculture-suitability_files/
├── data/
│     ├── average_annual_sst_2008.tif      # Yearly sst data
│     ├── average_annual_sst_2009.tif
│     ├── average_annual_sst_2010.tif
│     ├── average_annual_sst_2011.tif
│     ├── average_annual_sst_2012.tif
│     ├── depth.tif                        # Bathymetry data
│     └── wc_regions_clean.shp             # Economic zone data
├── scripts/
│     └── aqua_fun.R                       # Aquaculture suitability function
├── .gitignore
├── README.md                         
├── aquaculture-suitability.Rproj
├── aquaculture-suitability.html
└── aquaculture-suitability.qmd            # Complete analysis quarto document

```
## Data access
Data in this project were pulled from  
- Sea Surface Temperature data: [NOAA Coral Reef Watch](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php)
- Bathymetry data: [GEBCO Compilation Group](https://www.gebco.net/data_and_products/gridded_bathymetry_data/#area)
- Exclusive Economic Zone data: [Flanders Marine Institue](https://www.marineregions.org/eez.php)
- Species aquaculture data: [Sea Life Base](https://www.sealifebase.ca/search.php)

## References and Acknowledgements
All materials were created by [Ruth Oliver](https://github.com/ryoliver) for EDS-223. 

### Citations

- NOAA Coral Reef Watch. 2019, updated daily. NOAA Coral Reef Watch Version 3.1 Daily 5km Satellite Regional Virtual Station Time Series Data. College Park, Maryland, USA: NOAA Coral Reef Watch. Data set accessed 2024-11-20 at https://coralreefwatch.noaa.gov/product/vs/data.php.
- GEBCO Compilation Group (2022) GEBCO_2022 Grid Bathymetry Data. doi:10.5285/e0f0bb80-ab44-2739-e053-6c86abc0289c. 
- Flanders Marine Institute (2024): MarineRegions.org. Available online at www.marineregions.org. Consulted on 2024-11-30.
- Palomares, M.L.D. and D. Pauly. Editors. 2024. SeaLifeBase. World Wide Web electronic publication. www.sealifebase.org, version (08/2024).

