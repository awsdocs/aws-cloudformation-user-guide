# AWS::QuickSight::Template DateTimeFormatConfiguration<a name="aws-properties-quicksight-template-datetimeformatconfiguration"></a>

Formatting configuration for `DateTime` fields\.

## Syntax<a name="aws-properties-quicksight-template-datetimeformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-datetimeformatconfiguration-syntax.json"></a>

```
{
  "[DateTimeFormat](#cfn-quicksight-template-datetimeformatconfiguration-datetimeformat)" : String,
  "[NullValueFormatConfiguration](#cfn-quicksight-template-datetimeformatconfiguration-nullvalueformatconfiguration)" : NullValueFormatConfiguration,
  "[NumericFormatConfiguration](#cfn-quicksight-template-datetimeformatconfiguration-numericformatconfiguration)" : NumericFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-datetimeformatconfiguration-syntax.yaml"></a>

```
  [DateTimeFormat](#cfn-quicksight-template-datetimeformatconfiguration-datetimeformat): String
  [NullValueFormatConfiguration](#cfn-quicksight-template-datetimeformatconfiguration-nullvalueformatconfiguration): 
    NullValueFormatConfiguration
  [NumericFormatConfiguration](#cfn-quicksight-template-datetimeformatconfiguration-numericformatconfiguration): 
    NumericFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-template-datetimeformatconfiguration-properties"></a>

`DateTimeFormat`  <a name="cfn-quicksight-template-datetimeformatconfiguration-datetimeformat"></a>
Determines the `DateTime` format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullValueFormatConfiguration`  <a name="cfn-quicksight-template-datetimeformatconfiguration-nullvalueformatconfiguration"></a>
The options that determine the null value format configuration\.  
*Required*: No  
*Type*: [NullValueFormatConfiguration](aws-properties-quicksight-template-nullvalueformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericFormatConfiguration`  <a name="cfn-quicksight-template-datetimeformatconfiguration-numericformatconfiguration"></a>
The formatting configuration for numeric `DateTime` fields\.  
*Required*: No  
*Type*: [NumericFormatConfiguration](aws-properties-quicksight-template-numericformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)