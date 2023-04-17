# AWS::QuickSight::Dashboard PercentageDisplayFormatConfiguration<a name="aws-properties-quicksight-dashboard-percentagedisplayformatconfiguration"></a>

The options that determine the percentage display format configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-percentagedisplayformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-percentagedisplayformatconfiguration-syntax.json"></a>

```
{
  "[DecimalPlacesConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-decimalplacesconfiguration)" : DecimalPlacesConfiguration,
  "[NegativeValueConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-negativevalueconfiguration)" : NegativeValueConfiguration,
  "[NullValueFormatConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-nullvalueformatconfiguration)" : NullValueFormatConfiguration,
  "[Prefix](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-prefix)" : String,
  "[SeparatorConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-separatorconfiguration)" : NumericSeparatorConfiguration,
  "[Suffix](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-suffix)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-percentagedisplayformatconfiguration-syntax.yaml"></a>

```
  [DecimalPlacesConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-decimalplacesconfiguration): 
    DecimalPlacesConfiguration
  [NegativeValueConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-negativevalueconfiguration): 
    NegativeValueConfiguration
  [NullValueFormatConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-nullvalueformatconfiguration): 
    NullValueFormatConfiguration
  [Prefix](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-prefix): String
  [SeparatorConfiguration](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-separatorconfiguration): 
    NumericSeparatorConfiguration
  [Suffix](#cfn-quicksight-dashboard-percentagedisplayformatconfiguration-suffix): String
```

## Properties<a name="aws-properties-quicksight-dashboard-percentagedisplayformatconfiguration-properties"></a>

`DecimalPlacesConfiguration`  <a name="cfn-quicksight-dashboard-percentagedisplayformatconfiguration-decimalplacesconfiguration"></a>
The option that determines the decimal places configuration\.  
*Required*: No  
*Type*: [DecimalPlacesConfiguration](aws-properties-quicksight-dashboard-decimalplacesconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NegativeValueConfiguration`  <a name="cfn-quicksight-dashboard-percentagedisplayformatconfiguration-negativevalueconfiguration"></a>
The options that determine the negative value configuration\.  
*Required*: No  
*Type*: [NegativeValueConfiguration](aws-properties-quicksight-dashboard-negativevalueconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullValueFormatConfiguration`  <a name="cfn-quicksight-dashboard-percentagedisplayformatconfiguration-nullvalueformatconfiguration"></a>
The options that determine the null value format configuration\.  
*Required*: No  
*Type*: [NullValueFormatConfiguration](aws-properties-quicksight-dashboard-nullvalueformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-quicksight-dashboard-percentagedisplayformatconfiguration-prefix"></a>
Determines the prefix value of the percentage format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SeparatorConfiguration`  <a name="cfn-quicksight-dashboard-percentagedisplayformatconfiguration-separatorconfiguration"></a>
The options that determine the numeric separator configuration\.  
*Required*: No  
*Type*: [NumericSeparatorConfiguration](aws-properties-quicksight-dashboard-numericseparatorconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-quicksight-dashboard-percentagedisplayformatconfiguration-suffix"></a>
Determines the suffix value of the percentage format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)