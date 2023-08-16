# AWS::QuickSight::Template PercentageDisplayFormatConfiguration<a name="aws-properties-quicksight-template-percentagedisplayformatconfiguration"></a>

The options that determine the percentage display format configuration\.

## Syntax<a name="aws-properties-quicksight-template-percentagedisplayformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-percentagedisplayformatconfiguration-syntax.json"></a>

```
{
  "[DecimalPlacesConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-decimalplacesconfiguration)" : DecimalPlacesConfiguration,
  "[NegativeValueConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-negativevalueconfiguration)" : NegativeValueConfiguration,
  "[NullValueFormatConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-nullvalueformatconfiguration)" : NullValueFormatConfiguration,
  "[Prefix](#cfn-quicksight-template-percentagedisplayformatconfiguration-prefix)" : String,
  "[SeparatorConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-separatorconfiguration)" : NumericSeparatorConfiguration,
  "[Suffix](#cfn-quicksight-template-percentagedisplayformatconfiguration-suffix)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-percentagedisplayformatconfiguration-syntax.yaml"></a>

```
  [DecimalPlacesConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-decimalplacesconfiguration): 
    DecimalPlacesConfiguration
  [NegativeValueConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-negativevalueconfiguration): 
    NegativeValueConfiguration
  [NullValueFormatConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-nullvalueformatconfiguration): 
    NullValueFormatConfiguration
  [Prefix](#cfn-quicksight-template-percentagedisplayformatconfiguration-prefix): String
  [SeparatorConfiguration](#cfn-quicksight-template-percentagedisplayformatconfiguration-separatorconfiguration): 
    NumericSeparatorConfiguration
  [Suffix](#cfn-quicksight-template-percentagedisplayformatconfiguration-suffix): String
```

## Properties<a name="aws-properties-quicksight-template-percentagedisplayformatconfiguration-properties"></a>

`DecimalPlacesConfiguration`  <a name="cfn-quicksight-template-percentagedisplayformatconfiguration-decimalplacesconfiguration"></a>
The option that determines the decimal places configuration\.  
*Required*: No  
*Type*: [DecimalPlacesConfiguration](aws-properties-quicksight-template-decimalplacesconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NegativeValueConfiguration`  <a name="cfn-quicksight-template-percentagedisplayformatconfiguration-negativevalueconfiguration"></a>
The options that determine the negative value configuration\.  
*Required*: No  
*Type*: [NegativeValueConfiguration](aws-properties-quicksight-template-negativevalueconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullValueFormatConfiguration`  <a name="cfn-quicksight-template-percentagedisplayformatconfiguration-nullvalueformatconfiguration"></a>
The options that determine the null value format configuration\.  
*Required*: No  
*Type*: [NullValueFormatConfiguration](aws-properties-quicksight-template-nullvalueformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-quicksight-template-percentagedisplayformatconfiguration-prefix"></a>
Determines the prefix value of the percentage format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SeparatorConfiguration`  <a name="cfn-quicksight-template-percentagedisplayformatconfiguration-separatorconfiguration"></a>
The options that determine the numeric separator configuration\.  
*Required*: No  
*Type*: [NumericSeparatorConfiguration](aws-properties-quicksight-template-numericseparatorconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-quicksight-template-percentagedisplayformatconfiguration-suffix"></a>
Determines the suffix value of the percentage format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)