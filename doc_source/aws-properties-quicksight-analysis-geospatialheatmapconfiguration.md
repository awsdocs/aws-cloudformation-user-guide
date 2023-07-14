# AWS::QuickSight::Analysis GeospatialHeatmapConfiguration<a name="aws-properties-quicksight-analysis-geospatialheatmapconfiguration"></a>

The heatmap configuration of the geospatial point style\.

## Syntax<a name="aws-properties-quicksight-analysis-geospatialheatmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-geospatialheatmapconfiguration-syntax.json"></a>

```
{
  "[HeatmapColor](#cfn-quicksight-analysis-geospatialheatmapconfiguration-heatmapcolor)" : GeospatialHeatmapColorScale
}
```

### YAML<a name="aws-properties-quicksight-analysis-geospatialheatmapconfiguration-syntax.yaml"></a>

```
  [HeatmapColor](#cfn-quicksight-analysis-geospatialheatmapconfiguration-heatmapcolor): 
    GeospatialHeatmapColorScale
```

## Properties<a name="aws-properties-quicksight-analysis-geospatialheatmapconfiguration-properties"></a>

`HeatmapColor`  <a name="cfn-quicksight-analysis-geospatialheatmapconfiguration-heatmapcolor"></a>
The color scale specification for the heatmap point style\.  
*Required*: No  
*Type*: [GeospatialHeatmapColorScale](aws-properties-quicksight-analysis-geospatialheatmapcolorscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)