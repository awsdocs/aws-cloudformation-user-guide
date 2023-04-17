# AWS::QuickSight::Dashboard LineSeriesAxisDisplayOptions<a name="aws-properties-quicksight-dashboard-lineseriesaxisdisplayoptions"></a>

The series axis configuration of a line chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-lineseriesaxisdisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-lineseriesaxisdisplayoptions-syntax.json"></a>

```
{
  "[AxisOptions](#cfn-quicksight-dashboard-lineseriesaxisdisplayoptions-axisoptions)" : AxisDisplayOptions,
  "[MissingDataConfigurations](#cfn-quicksight-dashboard-lineseriesaxisdisplayoptions-missingdataconfigurations)" : [ MissingDataConfiguration, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-lineseriesaxisdisplayoptions-syntax.yaml"></a>

```
  [AxisOptions](#cfn-quicksight-dashboard-lineseriesaxisdisplayoptions-axisoptions): 
    AxisDisplayOptions
  [MissingDataConfigurations](#cfn-quicksight-dashboard-lineseriesaxisdisplayoptions-missingdataconfigurations): 
    - MissingDataConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-lineseriesaxisdisplayoptions-properties"></a>

`AxisOptions`  <a name="cfn-quicksight-dashboard-lineseriesaxisdisplayoptions-axisoptions"></a>
The options that determine the presentation of the line series axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MissingDataConfigurations`  <a name="cfn-quicksight-dashboard-lineseriesaxisdisplayoptions-missingdataconfigurations"></a>
The configuration options that determine how missing data is treated during the rendering of a line chart\.  
*Required*: No  
*Type*: List of [MissingDataConfiguration](aws-properties-quicksight-dashboard-missingdataconfiguration.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)