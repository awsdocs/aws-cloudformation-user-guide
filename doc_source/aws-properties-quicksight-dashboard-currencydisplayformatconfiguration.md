# AWS::QuickSight::Dashboard CurrencyDisplayFormatConfiguration<a name="aws-properties-quicksight-dashboard-currencydisplayformatconfiguration"></a>

The options that determine the currency display format configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-currencydisplayformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-currencydisplayformatconfiguration-syntax.json"></a>

```
{
  "[DecimalPlacesConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-decimalplacesconfiguration)" : DecimalPlacesConfiguration,
  "[NegativeValueConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-negativevalueconfiguration)" : NegativeValueConfiguration,
  "[NullValueFormatConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-nullvalueformatconfiguration)" : NullValueFormatConfiguration,
  "[NumberScale](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-numberscale)" : String,
  "[Prefix](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-prefix)" : String,
  "[SeparatorConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-separatorconfiguration)" : NumericSeparatorConfiguration,
  "[Suffix](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-suffix)" : String,
  "[Symbol](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-symbol)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-currencydisplayformatconfiguration-syntax.yaml"></a>

```
  [DecimalPlacesConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-decimalplacesconfiguration): 
    DecimalPlacesConfiguration
  [NegativeValueConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-negativevalueconfiguration): 
    NegativeValueConfiguration
  [NullValueFormatConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-nullvalueformatconfiguration): 
    NullValueFormatConfiguration
  [NumberScale](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-numberscale): String
  [Prefix](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-prefix): String
  [SeparatorConfiguration](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-separatorconfiguration): 
    NumericSeparatorConfiguration
  [Suffix](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-suffix): String
  [Symbol](#cfn-quicksight-dashboard-currencydisplayformatconfiguration-symbol): String
```

## Properties<a name="aws-properties-quicksight-dashboard-currencydisplayformatconfiguration-properties"></a>

`DecimalPlacesConfiguration`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-decimalplacesconfiguration"></a>
The option that determines the decimal places configuration\.  
*Required*: No  
*Type*: [DecimalPlacesConfiguration](aws-properties-quicksight-dashboard-decimalplacesconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NegativeValueConfiguration`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-negativevalueconfiguration"></a>
The options that determine the negative value configuration\.  
*Required*: No  
*Type*: [NegativeValueConfiguration](aws-properties-quicksight-dashboard-negativevalueconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullValueFormatConfiguration`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-nullvalueformatconfiguration"></a>
The options that determine the null value format configuration\.  
*Required*: No  
*Type*: [NullValueFormatConfiguration](aws-properties-quicksight-dashboard-nullvalueformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberScale`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-numberscale"></a>
Determines the number scale value for the currency format\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | BILLIONS | MILLIONS | NONE | THOUSANDS | TRILLIONS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-prefix"></a>
Determines the prefix value of the currency format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SeparatorConfiguration`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-separatorconfiguration"></a>
The options that determine the numeric separator configuration\.  
*Required*: No  
*Type*: [NumericSeparatorConfiguration](aws-properties-quicksight-dashboard-numericseparatorconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-suffix"></a>
Determines the suffix value of the currency format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Symbol`  <a name="cfn-quicksight-dashboard-currencydisplayformatconfiguration-symbol"></a>
Determines the symbol for the currency format\.  
*Required*: No  
*Type*: String  
*Pattern*: `[A-Z]{3}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)