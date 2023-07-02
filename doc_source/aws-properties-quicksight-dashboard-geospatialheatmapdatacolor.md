# AWS::QuickSight::Dashboard GeospatialHeatmapDataColor<a name="aws-properties-quicksight-dashboard-geospatialheatmapdatacolor"></a>

The color to be used in the heatmap point style\.

## Syntax<a name="aws-properties-quicksight-dashboard-geospatialheatmapdatacolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-geospatialheatmapdatacolor-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-dashboard-geospatialheatmapdatacolor-color)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-geospatialheatmapdatacolor-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-dashboard-geospatialheatmapdatacolor-color): String
```

## Properties<a name="aws-properties-quicksight-dashboard-geospatialheatmapdatacolor-properties"></a>

`Color`  <a name="cfn-quicksight-dashboard-geospatialheatmapdatacolor-color"></a>
The hex color to be used in the heatmap point style\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)