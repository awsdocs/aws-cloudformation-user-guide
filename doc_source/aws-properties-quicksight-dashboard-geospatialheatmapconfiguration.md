# AWS::QuickSight::Dashboard GeospatialHeatmapConfiguration<a name="aws-properties-quicksight-dashboard-geospatialheatmapconfiguration"></a>

The heatmap configuration of the geospatial point style\.

## Syntax<a name="aws-properties-quicksight-dashboard-geospatialheatmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-geospatialheatmapconfiguration-syntax.json"></a>

```
{
  "[HeatmapColor](#cfn-quicksight-dashboard-geospatialheatmapconfiguration-heatmapcolor)" : GeospatialHeatmapColorScale
}
```

### YAML<a name="aws-properties-quicksight-dashboard-geospatialheatmapconfiguration-syntax.yaml"></a>

```
  [HeatmapColor](#cfn-quicksight-dashboard-geospatialheatmapconfiguration-heatmapcolor): 
    GeospatialHeatmapColorScale
```

## Properties<a name="aws-properties-quicksight-dashboard-geospatialheatmapconfiguration-properties"></a>

`HeatmapColor`  <a name="cfn-quicksight-dashboard-geospatialheatmapconfiguration-heatmapcolor"></a>
The color scale specification for the heatmap point style\.  
*Required*: No  
*Type*: [GeospatialHeatmapColorScale](aws-properties-quicksight-dashboard-geospatialheatmapcolorscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)