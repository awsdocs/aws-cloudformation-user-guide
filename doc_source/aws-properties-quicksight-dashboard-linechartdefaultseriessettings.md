# AWS::QuickSight::Dashboard LineChartDefaultSeriesSettings<a name="aws-properties-quicksight-dashboard-linechartdefaultseriessettings"></a>

The options that determine the default presentation of all line series in `LineChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-linechartdefaultseriessettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-linechartdefaultseriessettings-syntax.json"></a>

```
{
  "[AxisBinding](#cfn-quicksight-dashboard-linechartdefaultseriessettings-axisbinding)" : String,
  "[LineStyleSettings](#cfn-quicksight-dashboard-linechartdefaultseriessettings-linestylesettings)" : LineChartLineStyleSettings,
  "[MarkerStyleSettings](#cfn-quicksight-dashboard-linechartdefaultseriessettings-markerstylesettings)" : LineChartMarkerStyleSettings
}
```

### YAML<a name="aws-properties-quicksight-dashboard-linechartdefaultseriessettings-syntax.yaml"></a>

```
  [AxisBinding](#cfn-quicksight-dashboard-linechartdefaultseriessettings-axisbinding): String
  [LineStyleSettings](#cfn-quicksight-dashboard-linechartdefaultseriessettings-linestylesettings): 
    LineChartLineStyleSettings
  [MarkerStyleSettings](#cfn-quicksight-dashboard-linechartdefaultseriessettings-markerstylesettings): 
    LineChartMarkerStyleSettings
```

## Properties<a name="aws-properties-quicksight-dashboard-linechartdefaultseriessettings-properties"></a>

`AxisBinding`  <a name="cfn-quicksight-dashboard-linechartdefaultseriessettings-axisbinding"></a>
The axis to which you are binding all line series to\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PRIMARY_YAXIS | SECONDARY_YAXIS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineStyleSettings`  <a name="cfn-quicksight-dashboard-linechartdefaultseriessettings-linestylesettings"></a>
Line styles options for all line series in the visual\.  
*Required*: No  
*Type*: [LineChartLineStyleSettings](aws-properties-quicksight-dashboard-linechartlinestylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MarkerStyleSettings`  <a name="cfn-quicksight-dashboard-linechartdefaultseriessettings-markerstylesettings"></a>
Marker styles options for all line series in the visual\.  
*Required*: No  
*Type*: [LineChartMarkerStyleSettings](aws-properties-quicksight-dashboard-linechartmarkerstylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)