# AWS::Location::Map MapConfiguration<a name="aws-properties-location-map-mapconfiguration"></a>

Specifies the map tile style selected from an available provider\.

## Syntax<a name="aws-properties-location-map-mapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-location-map-mapconfiguration-syntax.json"></a>

```
{
  "[Style](#cfn-location-map-mapconfiguration-style)" : String
}
```

### YAML<a name="aws-properties-location-map-mapconfiguration-syntax.yaml"></a>

```
  [Style](#cfn-location-map-mapconfiguration-style): String
```

## Properties<a name="aws-properties-location-map-mapconfiguration-properties"></a>

`Style`  <a name="cfn-location-map-mapconfiguration-style"></a>
Specifies the map style selected from an available data provider\.  
Valid [Esri map styles](https://docs.aws.amazon.com/location/latest/developerguide/esri.html):  
+ `VectorEsriDarkGrayCanvas` – The Esri Dark Gray Canvas map style\. A vector basemap with a dark gray, neutral background with minimal colors, labels, and features that's designed to draw attention to your thematic content\. 
+ `RasterEsriImagery` – The Esri Imagery map style\. A raster basemap that provides one meter or better satellite and aerial imagery in many parts of the world and lower resolution satellite imagery worldwide\. 
+ `VectorEsriLightGrayCanvas` – The Esri Light Gray Canvas map style, which provides a detailed vector basemap with a light gray, neutral background style with minimal colors, labels, and features that's designed to draw attention to your thematic content\. 
+ `VectorEsriTopographic` – The Esri Light map style, which provides a detailed vector basemap with a classic Esri map style\.
+ `VectorEsriStreets` – The Esri World Streets map style, which provides a detailed vector basemap for the world symbolized with a classic Esri street map style\. The vector tile layer is similar in content and style to the World Street Map raster map\.
+ `VectorEsriNavigation` – The Esri World Navigation map style, which provides a detailed basemap for the world symbolized with a custom navigation map style that's designed for use during the day in mobile devices\.
Valid [HERE Technologies map styles](https://docs.aws.amazon.com/location/latest/developerguide/HERE.html):  
+ `VectorHereContrast` – The HERE Contrast \(Berlin\) map style is a high contrast detailed base map of the world that blends 3D and 2D rendering\.
**Note**  
The `VectorHereContrast` style has been renamed from `VectorHereBerlin`\. `VectorHereBerlin` has been deprecated, but will continue to work in applications that use it\.
+ `VectorHereExplore` – A default HERE map style containing a neutral, global map and its features including roads, buildings, landmarks, and water features\. It also now includes a fully designed map of Japan\.
+ `VectorHereExploreTruck` – A global map containing truck restrictions and attributes \(e\.g\. width / height / HAZMAT\) symbolized with highlighted segments and icons on top of HERE Explore to support use cases within transport and logistics\.
+ `RasterHereExploreSatellite` – A global map containing high resolution satellite imagery\.
+ `HybridHereExploreSatellite` – A global map displaying the road network, street names, and city labels over satellite imagery\. This style will automatically retrieve both raster and vector tiles, and your charges will be based on total tiles retrieved\.
**Note**  
Hybrid styles use both vector and raster tiles when rendering the map that you see\. This means that more tiles are retrieved than when using either vector or raster tiles alone\. Your charges will include all tiles retrieved\.
Valid [GrabMaps map styles](https://docs.aws.amazon.com/location/latest/developerguide/grab.html):  
+ `VectorGrabStandardLight` – The Grab Standard Light map style provides a basemap with detailed land use coloring, area names, roads, landmarks, and points of interest covering Southeast Asia\.
+ `VectorGrabStandardDark` – The Grab Standard Dark map style provides a dark variation of the standard basemap covering Southeast Asia\.
Grab provides maps only for countries in Southeast Asia, and is only available in the Asia Pacific \(Singapore\) Region \(`ap-southeast-1`\)\. For more information, see [GrabMaps countries and area covered](https://docs.aws.amazon.com/location/latest/developerguide/grab.html#grab-coverage-area)\.
Valid [Open Data \(Preview\) map styles](https://docs.aws.amazon.com/location/latest/developerguide/open-data.html):  
+ `VectorOpenDataStandardLight` – The Open Data Standard Light \(preview\) map style provides a detailed basemap for the world suitable for website and mobile application use\. The map includes highways major roads, minor roads, railways, water features, cities, parks, landmarks, building footprints, and administrative boundaries\.
**Important**  
Open Data maps is in preview\. We may add, change, or remove features before announcing general availability\. For more information, see [Open Data is in preview release](https://docs.aws.amazon.com/location/latest/developerguide/open-data.html#open-data-preview)\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[-._\w]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)