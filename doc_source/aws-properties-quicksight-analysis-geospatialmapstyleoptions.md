# AWS::QuickSight::Analysis GeospatialMapStyleOptions<a name="aws-properties-quicksight-analysis-geospatialmapstyleoptions"></a>

The map style options of the geospatial map\.

## Syntax<a name="aws-properties-quicksight-analysis-geospatialmapstyleoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-geospatialmapstyleoptions-syntax.json"></a>

```
{
  "[BaseMapStyle](#cfn-quicksight-analysis-geospatialmapstyleoptions-basemapstyle)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-geospatialmapstyleoptions-syntax.yaml"></a>

```
  [BaseMapStyle](#cfn-quicksight-analysis-geospatialmapstyleoptions-basemapstyle): String
```

## Properties<a name="aws-properties-quicksight-analysis-geospatialmapstyleoptions-properties"></a>

`BaseMapStyle`  <a name="cfn-quicksight-analysis-geospatialmapstyleoptions-basemapstyle"></a>
The base map style of the geospatial map\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DARK_GRAY | IMAGERY | LIGHT_GRAY | STREET`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)