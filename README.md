# Tourist Maps using MapBox GL JS

## Aim

This is an interface that provides tourists visiting Melbourne a comprehensive and interactive platform to view all the go-to places within Melbourne. The interface mainly uses MapBox GL JS and HTML5. 

The features are as follows - 
- Provides nearest tram stop and train station when a point of interest is clicked.

- Points of Interest have been categorised into 4 categories namely Age, Time of Day, Duration and Theme.

- Provides detailed information about the POI, tram stop and train station when hovered over.

- Displays tram routes within Melbourne to determine which route the tram stop falls under.

## Design

- **Pre-requisites** :
 
  1. A base layer map was created with Tram Routes within Melbourne using [MapBox Studio](https://www.mapbox.com/mapbox-studio).
  
  2. All the shapefiles of POI, Tram Stops and Train Stations were converted into GEOJSON files for ease of use using [ArcGIS Pro](https://pro.arcgis.com/en/pro-app/get-started/get-started.htm#:~:text=ArcGIS%20Pro%20is%20the%20latest,Online%20or%20ArcGIS%20Enterprise%20portal).
  
- **Interface Implementation** : 

  1. The POIs, tram stops and train stations were displayed on the base map using the inbuilt functions of [MapBox GL JS](https://docs.mapbox.com/mapbox-gl-js/api/)   specifcially map.addSource() and map.addLayer().
  
  2. The nearest tram stop and train station was computed using [Turf.js](https://docs.mapbox.com/help/glossary/turf/) and its inbuilt function turf.nearest().
  
  3. Lastly, the fileration of categories was done using the Filter attribute of map.addLayer() and ‘change’ event listener. Refer to this [link](https://docs.mapbox.com/mapbox-gl-js/example/filter-markers/) for more information. The interface files also contain a similar code. 
  
- **Interface styling** : 

  1. Finally, the interface was styled using CSS. Please refer file tourist.css for more information on the styling. 

## How to use the interface ?

1. index.html is the home page of the interface that contains buttons that display individual maps as per the categories when clicked.

2. Each button displays a map below with a legend on the left. The map contains a toggle list of various options on the top right corner through which tourists can navigate the map. 

3. Click on a point of interest to view the nearest tram stop highlighted in red and nearest train station highlighted in purple. 

4. Hover over any POI, tram stop or train station to view more information about the same.

5. Instructions on how to use the interface can be found on the home page itself below the buttons. 

