# AWS::QuickSight::Dashboard GeospatialWindowOptions<a name="aws-properties-quicksight-dashboard-geospatialwindowoptions"></a>

The window options of the geospatial map visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-geospatialwindowoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-geospatialwindowoptions-syntax.json"></a>

```
{
  "[Bounds](#cfn-quicksight-dashboard-geospatialwindowoptions-bounds)" : GeospatialCoordinateBounds,
  "[MapZoomMode](#cfn-quicksight-dashboard-geospatialwindowoptions-mapzoommode)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-geospatialwindowoptions-syntax.yaml"></a>

```
  [Bounds](#cfn-quicksight-dashboard-geospatialwindowoptions-bounds): 
    GeospatialCoordinateBounds
  [MapZoomMode](#cfn-quicksight-dashboard-geospatialwindowoptions-mapzoommode): String
```

## Properties<a name="aws-properties-quicksight-dashboard-geospatialwindowoptions-properties"></a>

`Bounds`  <a name="cfn-quicksight-dashboard-geospatialwindowoptions-bounds"></a>
The bounds options \(north, south, west, east\) of the geospatial window options\.  
*Required*: No  
*Type*: [GeospatialCoordinateBounds](aws-properties-quicksight-dashboard-geospatialcoordinatebounds.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapZoomMode`  <a name="cfn-quicksight-dashboard-geospatialwindowoptions-mapzoommode"></a>
The map zoom modes \(manual, auto\) of the geospatial window options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | MANUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)