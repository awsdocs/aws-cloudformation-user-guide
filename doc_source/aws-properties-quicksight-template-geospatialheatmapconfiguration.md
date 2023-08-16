# AWS::QuickSight::Template GeospatialHeatmapConfiguration<a name="aws-properties-quicksight-template-geospatialheatmapconfiguration"></a>

The heatmap configuration of the geospatial point style\.

## Syntax<a name="aws-properties-quicksight-template-geospatialheatmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-geospatialheatmapconfiguration-syntax.json"></a>

```
{
  "[HeatmapColor](#cfn-quicksight-template-geospatialheatmapconfiguration-heatmapcolor)" : GeospatialHeatmapColorScale
}
```

### YAML<a name="aws-properties-quicksight-template-geospatialheatmapconfiguration-syntax.yaml"></a>

```
  [HeatmapColor](#cfn-quicksight-template-geospatialheatmapconfiguration-heatmapcolor): 
    GeospatialHeatmapColorScale
```

## Properties<a name="aws-properties-quicksight-template-geospatialheatmapconfiguration-properties"></a>

`HeatmapColor`  <a name="cfn-quicksight-template-geospatialheatmapconfiguration-heatmapcolor"></a>
The color scale specification for the heatmap point style\.  
*Required*: No  
*Type*: [GeospatialHeatmapColorScale](aws-properties-quicksight-template-geospatialheatmapcolorscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)