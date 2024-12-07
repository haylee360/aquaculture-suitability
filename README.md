# Identifying Coastal Areas Best Suited for Potential Aquaculture Investment
![aquaculture-image](https://i0.wp.com/calmatters.org/wp-content/uploads/2020/05/NOAA_Mussellonglines_02.jpg?fit=1200%2C799&ssl=1)
Source : [Cal Matters](https://calmatters.org/environment/2020/05/california-shellfish-farming-aquaculture/)

This repository houses a function that generates a map of suitable habitats along the West Coast of the United States for potential aquaculture species. The calculation is based on the species of interest's suitable range of sea surface temperature (sst) and suitable range of depth below the sea level. The complete function is presented at the top of the document and the workflow for creating the function is explained in detail below. 

## Skills
This analysis highlights

- Working with vector data using `sf`
- Working with raster data using `terra`
- Working with census data, bathymetry data, and 
- Vector algebra and data cleaning
- Mapmaking, plotting, and data visualization using `tmap` and `ggplot`

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
- [US EPA's EJSCREEN tool](https://www.epa.gov/ejscreen/download-ejscreen-data)
- HOLC redlining data from the [Digital Scholarship Lab](https://dsl.richmond.edu/panorama/redlining/#loc=5/39.1/-94.58&text=downloads)
- Bird diversity observations from the [Global Biodiversity Information Facility](https://eds-223-geospatial.github.io/assignments/gbif.org)

All relevant data available [here](https://drive.google.com/file/d/14CauXFZkVh_6z2Euq0m1Sq1kHQ31fiMk/view?usp=drive_link).

## References and Acknowledgements
All materials were created by [Ruth Oliver](https://github.com/ryoliver) for EDS-223. 

### Citations

- Global Biodiversity Information Facility, GBIF.org (13 October 2024) GBIF Occurence Download. 
- HOLC Redlining Data. Nelson, R. K., Winling, L, et al. (2023). Mapping Inequality: Redlining in New Deal America. Digital Scholarship Lab. https://dsl.richmond.edu/panorama/redlining 
- EJScreen: Environmental Justice Screening and Mapping Tool. United States Environmental Protection Agency. 2024 version. EJScreen. Retrieved: 10/4/24 from www.epa.gov/ejscreen. 
