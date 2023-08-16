# AWS::QuickSight::Dashboard StringFormatConfiguration<a name="aws-properties-quicksight-dashboard-stringformatconfiguration"></a>

Formatting configuration for string fields\.

## Syntax<a name="aws-properties-quicksight-dashboard-stringformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-stringformatconfiguration-syntax.json"></a>

```
{
  "[NullValueFormatConfiguration](#cfn-quicksight-dashboard-stringformatconfiguration-nullvalueformatconfiguration)" : NullValueFormatConfiguration,
  "[NumericFormatConfiguration](#cfn-quicksight-dashboard-stringformatconfiguration-numericformatconfiguration)" : NumericFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-stringformatconfiguration-syntax.yaml"></a>

```
  [NullValueFormatConfiguration](#cfn-quicksight-dashboard-stringformatconfiguration-nullvalueformatconfiguration): 
    NullValueFormatConfiguration
  [NumericFormatConfiguration](#cfn-quicksight-dashboard-stringformatconfiguration-numericformatconfiguration): 
    NumericFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-stringformatconfiguration-properties"></a>

`NullValueFormatConfiguration`  <a name="cfn-quicksight-dashboard-stringformatconfiguration-nullvalueformatconfiguration"></a>
The options that determine the null value format configuration\.  
*Required*: No  
*Type*: [NullValueFormatConfiguration](aws-properties-quicksight-dashboard-nullvalueformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericFormatConfiguration`  <a name="cfn-quicksight-dashboard-stringformatconfiguration-numericformatconfiguration"></a>
The formatting configuration for numeric strings\.  
*Required*: No  
*Type*: [NumericFormatConfiguration](aws-properties-quicksight-dashboard-numericformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)