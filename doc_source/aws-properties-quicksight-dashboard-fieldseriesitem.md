# AWS::QuickSight::Dashboard FieldSeriesItem<a name="aws-properties-quicksight-dashboard-fieldseriesitem"></a>

The field series item configuration of a line chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-fieldseriesitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-fieldseriesitem-syntax.json"></a>

```
{
  "[AxisBinding](#cfn-quicksight-dashboard-fieldseriesitem-axisbinding)" : String,
  "[FieldId](#cfn-quicksight-dashboard-fieldseriesitem-fieldid)" : String,
  "[Settings](#cfn-quicksight-dashboard-fieldseriesitem-settings)" : LineChartSeriesSettings
}
```

### YAML<a name="aws-properties-quicksight-dashboard-fieldseriesitem-syntax.yaml"></a>

```
  [AxisBinding](#cfn-quicksight-dashboard-fieldseriesitem-axisbinding): String
  [FieldId](#cfn-quicksight-dashboard-fieldseriesitem-fieldid): String
  [Settings](#cfn-quicksight-dashboard-fieldseriesitem-settings): 
    LineChartSeriesSettings
```

## Properties<a name="aws-properties-quicksight-dashboard-fieldseriesitem-properties"></a>

`AxisBinding`  <a name="cfn-quicksight-dashboard-fieldseriesitem-axisbinding"></a>
The axis that you are binding the field to\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `PRIMARY_YAXIS | SECONDARY_YAXIS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-dashboard-fieldseriesitem-fieldid"></a>
The field ID of the field for which you are setting the axis binding\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Settings`  <a name="cfn-quicksight-dashboard-fieldseriesitem-settings"></a>
The options that determine the presentation of line series associated to the field\.  
*Required*: No  
*Type*: [LineChartSeriesSettings](aws-properties-quicksight-dashboard-linechartseriessettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)