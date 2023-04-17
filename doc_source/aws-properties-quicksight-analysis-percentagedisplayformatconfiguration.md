# AWS::QuickSight::Analysis PercentageDisplayFormatConfiguration<a name="aws-properties-quicksight-analysis-percentagedisplayformatconfiguration"></a>

The options that determine the percentage display format configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-percentagedisplayformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-percentagedisplayformatconfiguration-syntax.json"></a>

```
{
  "[DecimalPlacesConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-decimalplacesconfiguration)" : DecimalPlacesConfiguration,
  "[NegativeValueConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-negativevalueconfiguration)" : NegativeValueConfiguration,
  "[NullValueFormatConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-nullvalueformatconfiguration)" : NullValueFormatConfiguration,
  "[Prefix](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-prefix)" : String,
  "[SeparatorConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-separatorconfiguration)" : NumericSeparatorConfiguration,
  "[Suffix](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-suffix)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-percentagedisplayformatconfiguration-syntax.yaml"></a>

```
  [DecimalPlacesConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-decimalplacesconfiguration): 
    DecimalPlacesConfiguration
  [NegativeValueConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-negativevalueconfiguration): 
    NegativeValueConfiguration
  [NullValueFormatConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-nullvalueformatconfiguration): 
    NullValueFormatConfiguration
  [Prefix](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-prefix): String
  [SeparatorConfiguration](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-separatorconfiguration): 
    NumericSeparatorConfiguration
  [Suffix](#cfn-quicksight-analysis-percentagedisplayformatconfiguration-suffix): String
```

## Properties<a name="aws-properties-quicksight-analysis-percentagedisplayformatconfiguration-properties"></a>

`DecimalPlacesConfiguration`  <a name="cfn-quicksight-analysis-percentagedisplayformatconfiguration-decimalplacesconfiguration"></a>
The option that determines the decimal places configuration\.  
*Required*: No  
*Type*: [DecimalPlacesConfiguration](aws-properties-quicksight-analysis-decimalplacesconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NegativeValueConfiguration`  <a name="cfn-quicksight-analysis-percentagedisplayformatconfiguration-negativevalueconfiguration"></a>
The options that determine the negative value configuration\.  
*Required*: No  
*Type*: [NegativeValueConfiguration](aws-properties-quicksight-analysis-negativevalueconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullValueFormatConfiguration`  <a name="cfn-quicksight-analysis-percentagedisplayformatconfiguration-nullvalueformatconfiguration"></a>
The options that determine the null value format configuration\.  
*Required*: No  
*Type*: [NullValueFormatConfiguration](aws-properties-quicksight-analysis-nullvalueformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-quicksight-analysis-percentagedisplayformatconfiguration-prefix"></a>
Determines the prefix value of the percentage format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SeparatorConfiguration`  <a name="cfn-quicksight-analysis-percentagedisplayformatconfiguration-separatorconfiguration"></a>
The options that determine the numeric separator configuration\.  
*Required*: No  
*Type*: [NumericSeparatorConfiguration](aws-properties-quicksight-analysis-numericseparatorconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-quicksight-analysis-percentagedisplayformatconfiguration-suffix"></a>
Determines the suffix value of the percentage format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)