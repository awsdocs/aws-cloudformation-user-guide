# AWS::QuickSight::Template LineChartDefaultSeriesSettings<a name="aws-properties-quicksight-template-linechartdefaultseriessettings"></a>

The options that determine the default presentation of all line series in `LineChartVisual`\.

## Syntax<a name="aws-properties-quicksight-template-linechartdefaultseriessettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-linechartdefaultseriessettings-syntax.json"></a>

```
{
  "[AxisBinding](#cfn-quicksight-template-linechartdefaultseriessettings-axisbinding)" : String,
  "[LineStyleSettings](#cfn-quicksight-template-linechartdefaultseriessettings-linestylesettings)" : LineChartLineStyleSettings,
  "[MarkerStyleSettings](#cfn-quicksight-template-linechartdefaultseriessettings-markerstylesettings)" : LineChartMarkerStyleSettings
}
```

### YAML<a name="aws-properties-quicksight-template-linechartdefaultseriessettings-syntax.yaml"></a>

```
  [AxisBinding](#cfn-quicksight-template-linechartdefaultseriessettings-axisbinding): String
  [LineStyleSettings](#cfn-quicksight-template-linechartdefaultseriessettings-linestylesettings): 
    LineChartLineStyleSettings
  [MarkerStyleSettings](#cfn-quicksight-template-linechartdefaultseriessettings-markerstylesettings): 
    LineChartMarkerStyleSettings
```

## Properties<a name="aws-properties-quicksight-template-linechartdefaultseriessettings-properties"></a>

`AxisBinding`  <a name="cfn-quicksight-template-linechartdefaultseriessettings-axisbinding"></a>
The axis to which you are binding all line series to\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PRIMARY_YAXIS | SECONDARY_YAXIS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineStyleSettings`  <a name="cfn-quicksight-template-linechartdefaultseriessettings-linestylesettings"></a>
Line styles options for all line series in the visual\.  
*Required*: No  
*Type*: [LineChartLineStyleSettings](aws-properties-quicksight-template-linechartlinestylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MarkerStyleSettings`  <a name="cfn-quicksight-template-linechartdefaultseriessettings-markerstylesettings"></a>
Marker styles options for all line series in the visual\.  
*Required*: No  
*Type*: [LineChartMarkerStyleSettings](aws-properties-quicksight-template-linechartmarkerstylesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)