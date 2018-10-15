# Residential demolitions in Austin

This data and analysis supports an Austin American-Statesman [article](https://www.statesman.com/news/20181012/in-austin-home-demolitions-soar-along-with-economic-fortunes) by Phil Jankowski about residential demolitions in Austin.

## Analysis

The data processing and analysis is done Jupyter Notebook files in the folder `/notebooks/`. There is one notebook that pulls down filtered Construction Permits data from the city's data portal and processes it. There are others that look a full-home demolitions, partial demolitions and the contractors who perform them.

The notebooks are heavily annotated to inform how we went about our work. They include visualizations and findings. 

## Print graphics

Among the outputs of the notebooks are data to support two print graphics: a Line chart of demolitions per year by zip code and a map of ZIP code areas with most demolitions from 2008 to 2017.

### Demos by year, by zip

- Data is: `data-processed/top_demos_year_zip.csv`.
- Example: `resources/top_demos_yr_zip_example.png`.
- [Interactive example in Tableau](https://public.tableau.com/profile/statcomdata#!/vizhome/Demolitions2008-2017/DemolitionsbyZIP).

### Demos map

- Data is: `data-processed/demos_by_zip.csv`
- Example map: `qgis/demos_by_zip.pdf`

Example map was created in QGIS. Some files used but not tracked in this repository:

- City of Austin [Street Centerline shapefile](https://data.austintexas.gov/Locations-and-Maps/Street-Centerlines/m5w3-uea6).
- TIGER/Line Shapefiles 2017 [ZIP Code Tabulation Areas](https://www.census.gov/cgi-bin/geo/shapefiles/index.php)
