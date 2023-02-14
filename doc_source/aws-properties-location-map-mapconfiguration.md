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
Valid styles: `VectorEsriStreets`, `VectorEsriTopographic`, `VectorEsriNavigation`, `VectorEsriDarkGrayCanvas`, `VectorEsriLightGrayCanvas`, `VectorHereBerlin`\.  
When using HERE as your data provider, and selecting the Style `VectorHereBerlin`, you may not use HERE Technologies maps for Asset Management\. See the [AWS Service Terms](http://aws.amazon.com/service-terms/) for Amazon Location Service\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[-._\w]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)