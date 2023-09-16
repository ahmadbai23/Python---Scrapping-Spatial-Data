# Scraping Spatial Data

This project involves retrieving spatial data from the OpenStreetMap website, followed by data cleansing, and then creating visualizations using marker clustering.
The libraries I used for this project are:

- osmnx: Used for scraping features from the OpenStreetMap website.
- geopandas: Used for creating boundaries as polygons.
- pandas: Used for data checking and cleansing.
- folium: Used for visualizing the data on a map.

# Data :
- Boundary_DKI_Jakarta.geojson = polygon area of interest
- before.html = marker visualize
- after.html = marker cluster visualize

# 1. Preparation and Data Scraping
In this phase, the steps involved are to prepare the area of interest for the location where data scraping will be performed (boundaries). In this case, I have included the data I used, which is the boundary of DKI Jakarta as the area of interest.
If you wish to use your own spatial data, you can download the data from the [tanahairgeoportal](https://tanahair.indonesia.go.id/portal-web) (shapefile format) or from [geojson.io](http://geojson.io/#map=2/0/20) On this website, you can create your own polygon according to your preferences and export the data in geojson format.

# 2. Data Checking and Cleansing

After we have retrieved the data, we perform data cleansing by removing null values and using only the necessary fields. In this case, I'm extracting only two fields: name and geometry (location).

Upon checking the geometry data type, we found that the data retrieved has inconsistent geometry types such as point, polygon, and multi polygon. Therefore, we need to standardize the geometry data type by converting all of them to points.

# 3. Visualization with Folium

Once the data is clean and ready for visualization, the next step is to plot these points on a map using the Folium library. The first thing to consider is to find the coordinates for the location you want to use as a map. You can obtain these coordinates from [Google Maps](https://www.google.com/maps/) and set an appropriate zoom level.

After having the base map, the final step is to create markers for each point, allowing them to be displayed on the previously created base map.

Please let me know if you have any further questions or need additional assistance with your project!

