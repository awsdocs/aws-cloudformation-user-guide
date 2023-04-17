# AWS::QuickSight::Template GeospatialWindowOptions<a name="aws-properties-quicksight-template-geospatialwindowoptions"></a>

The window options of the geospatial map visual\.

## Syntax<a name="aws-properties-quicksight-template-geospatialwindowoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-geospatialwindowoptions-syntax.json"></a>

```
{
  "[Bounds](#cfn-quicksight-template-geospatialwindowoptions-bounds)" : GeospatialCoordinateBounds,
  "[MapZoomMode](#cfn-quicksight-template-geospatialwindowoptions-mapzoommode)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-geospatialwindowoptions-syntax.yaml"></a>

```
  [Bounds](#cfn-quicksight-template-geospatialwindowoptions-bounds): 
    GeospatialCoordinateBounds
  [MapZoomMode](#cfn-quicksight-template-geospatialwindowoptions-mapzoommode): String
```

## Properties<a name="aws-properties-quicksight-template-geospatialwindowoptions-properties"></a>

`Bounds`  <a name="cfn-quicksight-template-geospatialwindowoptions-bounds"></a>
The bounds options \(north, south, west, east\) of the geospatial window options\.  
*Required*: No  
*Type*: [GeospatialCoordinateBounds](aws-properties-quicksight-template-geospatialcoordinatebounds.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapZoomMode`  <a name="cfn-quicksight-template-geospatialwindowoptions-mapzoommode"></a>
The map zoom modes \(manual, auto\) of the geospatial window options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | MANUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)