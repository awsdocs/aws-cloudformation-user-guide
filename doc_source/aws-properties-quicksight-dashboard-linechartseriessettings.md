# AWS::QuickSight::Dashboard LineChartSeriesSettings<a name="aws-properties-quicksight-dashboard-linechartseriessettings"></a>

The options that determine the presentation of a line series in the visual

## Syntax<a name="aws-properties-quicksight-dashboard-linechartseriessettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-linechartseriessettings-syntax.json"></a>

```
{
  "[LineStyleSettings](#cfn-quicksight-dashboard-linechartseriessettings-linestylesettings)" : LineChartLineStyleSettings,
  "[MarkerStyleSettings](#cfn-quicksight-dashboard-linechartseriessettings-markerstylesettings)" : LineChartMarkerStyleSettings
}
```

### YAML<a name="aws-properties-quicksight-dashboard-linechartseriessettings-syntax.yaml"></a>

```
  [LineStyleSettings](#cfn-quicksight-dashboard-linechartseriessettings-linestylesettings): 
    LineChartLineStyleSettings
  [MarkerStyleSettings](#cfn-quicksight-dashboard-linechartseriessettings-markerstylesettings): 
    LineChartMarkerStyleSettings
```

## Properties<a name="aws-properties-quicksight-dashboard-linechartseriessettings-properties"></a>

`LineStyleSettings`  <a name="cfn-quicksight-dashboard-linechartseriessettings-linestylesettings"></a>
Line styles options for a line series in `LineChartVisual`\.  
*Required*: No  
*Type*: [LineChartLineStyleSettings](aws-properties-quicksight-dashboard-linechartlinestylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MarkerStyleSettings`  <a name="cfn-quicksight-dashboard-linechartseriessettings-markerstylesettings"></a>
Marker styles options for a line series in `LineChartVisual`\.  
*Required*: No  
*Type*: [LineChartMarkerStyleSettings](aws-properties-quicksight-dashboard-linechartmarkerstylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)