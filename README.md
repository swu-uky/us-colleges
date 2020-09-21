# Colleges in the US

## Data

    Data obtained from *Homeland Infrastructure Foundation-Level Data* at:

    https://hifld-geoplatform.opendata.arcgis.com/datasets/colleges-and-universities?geometry=-129.088%2C26.603%2C-62.335%2C39.448

## Process

1.  After downloading the shapefile, used the command prompt to clean up the data using the command:

    mapshaper data/Colleges_and_Universities-shp/Colleges_and_Universities.shp -proj wgs84 -filter-fields NAME,CITY,STATE,TOT_ENROLL -o format=geojson data/colleges.json -verbose

2.  Further data processing in QGIS removing unneeded entries

3.  Loosely followed a Mapbox Tutorial to get the map started with final data:

    https://docs.mapbox.com/help/tutorials/create-interactive-hover-effects-with-mapbox-gl-js/

4.  Incorporated other Mapbox GL JS examples to add to map:

    https://docs.mapbox.com/mapbox-gl-js/example/setstyle/

    https://docs.mapbox.com/mapbox-gl-js/example/mapbox-gl-geocoder/

    https://docs.mapbox.com/mapbox-gl-js/example/flyto/