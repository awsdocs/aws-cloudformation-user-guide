# AWS::QuickSight::Analysis GeospatialWindowOptions<a name="aws-properties-quicksight-analysis-geospatialwindowoptions"></a>

The window options of the geospatial map visual\.

## Syntax<a name="aws-properties-quicksight-analysis-geospatialwindowoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-geospatialwindowoptions-syntax.json"></a>

```
{
  "[Bounds](#cfn-quicksight-analysis-geospatialwindowoptions-bounds)" : GeospatialCoordinateBounds,
  "[MapZoomMode](#cfn-quicksight-analysis-geospatialwindowoptions-mapzoommode)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-geospatialwindowoptions-syntax.yaml"></a>

```
  [Bounds](#cfn-quicksight-analysis-geospatialwindowoptions-bounds): 
    GeospatialCoordinateBounds
  [MapZoomMode](#cfn-quicksight-analysis-geospatialwindowoptions-mapzoommode): String
```

## Properties<a name="aws-properties-quicksight-analysis-geospatialwindowoptions-properties"></a>

`Bounds`  <a name="cfn-quicksight-analysis-geospatialwindowoptions-bounds"></a>
The bounds options \(north, south, west, east\) of the geospatial window options\.  
*Required*: No  
*Type*: [GeospatialCoordinateBounds](aws-properties-quicksight-analysis-geospatialcoordinatebounds.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapZoomMode`  <a name="cfn-quicksight-analysis-geospatialwindowoptions-mapzoommode"></a>
The map zoom modes \(manual, auto\) of the geospatial window options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | MANUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)