# AWS::QuickSight::Analysis LineChartSeriesSettings<a name="aws-properties-quicksight-analysis-linechartseriessettings"></a>

The options that determine the presentation of a line series in the visual

## Syntax<a name="aws-properties-quicksight-analysis-linechartseriessettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-linechartseriessettings-syntax.json"></a>

```
{
  "[LineStyleSettings](#cfn-quicksight-analysis-linechartseriessettings-linestylesettings)" : LineChartLineStyleSettings,
  "[MarkerStyleSettings](#cfn-quicksight-analysis-linechartseriessettings-markerstylesettings)" : LineChartMarkerStyleSettings
}
```

### YAML<a name="aws-properties-quicksight-analysis-linechartseriessettings-syntax.yaml"></a>

```
  [LineStyleSettings](#cfn-quicksight-analysis-linechartseriessettings-linestylesettings): 
    LineChartLineStyleSettings
  [MarkerStyleSettings](#cfn-quicksight-analysis-linechartseriessettings-markerstylesettings): 
    LineChartMarkerStyleSettings
```

## Properties<a name="aws-properties-quicksight-analysis-linechartseriessettings-properties"></a>

`LineStyleSettings`  <a name="cfn-quicksight-analysis-linechartseriessettings-linestylesettings"></a>
Line styles options for a line series in `LineChartVisual`\.  
*Required*: No  
*Type*: [LineChartLineStyleSettings](aws-properties-quicksight-analysis-linechartlinestylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MarkerStyleSettings`  <a name="cfn-quicksight-analysis-linechartseriessettings-markerstylesettings"></a>
Marker styles options for a line series in `LineChartVisual`\.  
*Required*: No  
*Type*: [LineChartMarkerStyleSettings](aws-properties-quicksight-analysis-linechartmarkerstylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)