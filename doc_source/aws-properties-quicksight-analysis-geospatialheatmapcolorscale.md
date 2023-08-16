# AWS::QuickSight::Analysis GeospatialHeatmapColorScale<a name="aws-properties-quicksight-analysis-geospatialheatmapcolorscale"></a>

The color scale specification for the heatmap point style\.

## Syntax<a name="aws-properties-quicksight-analysis-geospatialheatmapcolorscale-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-geospatialheatmapcolorscale-syntax.json"></a>

```
{
  "[Colors](#cfn-quicksight-analysis-geospatialheatmapcolorscale-colors)" : [ GeospatialHeatmapDataColor, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-geospatialheatmapcolorscale-syntax.yaml"></a>

```
  [Colors](#cfn-quicksight-analysis-geospatialheatmapcolorscale-colors): 
    - GeospatialHeatmapDataColor
```

## Properties<a name="aws-properties-quicksight-analysis-geospatialheatmapcolorscale-properties"></a>

`Colors`  <a name="cfn-quicksight-analysis-geospatialheatmapcolorscale-colors"></a>
The list of colors to be used in heatmap point style\.  
*Required*: No  
*Type*: List of [GeospatialHeatmapDataColor](aws-properties-quicksight-analysis-geospatialheatmapdatacolor.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)