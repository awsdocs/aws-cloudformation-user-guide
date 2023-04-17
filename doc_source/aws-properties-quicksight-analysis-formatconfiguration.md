# AWS::QuickSight::Analysis FormatConfiguration<a name="aws-properties-quicksight-analysis-formatconfiguration"></a>

The formatting configuration for all types of field\.

## Syntax<a name="aws-properties-quicksight-analysis-formatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-formatconfiguration-syntax.json"></a>

```
{
  "[DateTimeFormatConfiguration](#cfn-quicksight-analysis-formatconfiguration-datetimeformatconfiguration)" : DateTimeFormatConfiguration,
  "[NumberFormatConfiguration](#cfn-quicksight-analysis-formatconfiguration-numberformatconfiguration)" : NumberFormatConfiguration,
  "[StringFormatConfiguration](#cfn-quicksight-analysis-formatconfiguration-stringformatconfiguration)" : StringFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-formatconfiguration-syntax.yaml"></a>

```
  [DateTimeFormatConfiguration](#cfn-quicksight-analysis-formatconfiguration-datetimeformatconfiguration): 
    DateTimeFormatConfiguration
  [NumberFormatConfiguration](#cfn-quicksight-analysis-formatconfiguration-numberformatconfiguration): 
    NumberFormatConfiguration
  [StringFormatConfiguration](#cfn-quicksight-analysis-formatconfiguration-stringformatconfiguration): 
    StringFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-formatconfiguration-properties"></a>

`DateTimeFormatConfiguration`  <a name="cfn-quicksight-analysis-formatconfiguration-datetimeformatconfiguration"></a>
Formatting configuration for `DateTime` fields\.  
*Required*: No  
*Type*: [DateTimeFormatConfiguration](aws-properties-quicksight-analysis-datetimeformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberFormatConfiguration`  <a name="cfn-quicksight-analysis-formatconfiguration-numberformatconfiguration"></a>
Formatting configuration for number fields\.  
*Required*: No  
*Type*: [NumberFormatConfiguration](aws-properties-quicksight-analysis-numberformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringFormatConfiguration`  <a name="cfn-quicksight-analysis-formatconfiguration-stringformatconfiguration"></a>
Formatting configuration for string fields\.  
*Required*: No  
*Type*: [StringFormatConfiguration](aws-properties-quicksight-analysis-stringformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)