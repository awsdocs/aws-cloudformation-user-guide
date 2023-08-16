# AWS::QuickSight::Template CurrencyDisplayFormatConfiguration<a name="aws-properties-quicksight-template-currencydisplayformatconfiguration"></a>

The options that determine the currency display format configuration\.

## Syntax<a name="aws-properties-quicksight-template-currencydisplayformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-currencydisplayformatconfiguration-syntax.json"></a>

```
{
  "[DecimalPlacesConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-decimalplacesconfiguration)" : DecimalPlacesConfiguration,
  "[NegativeValueConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-negativevalueconfiguration)" : NegativeValueConfiguration,
  "[NullValueFormatConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-nullvalueformatconfiguration)" : NullValueFormatConfiguration,
  "[NumberScale](#cfn-quicksight-template-currencydisplayformatconfiguration-numberscale)" : String,
  "[Prefix](#cfn-quicksight-template-currencydisplayformatconfiguration-prefix)" : String,
  "[SeparatorConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-separatorconfiguration)" : NumericSeparatorConfiguration,
  "[Suffix](#cfn-quicksight-template-currencydisplayformatconfiguration-suffix)" : String,
  "[Symbol](#cfn-quicksight-template-currencydisplayformatconfiguration-symbol)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-currencydisplayformatconfiguration-syntax.yaml"></a>

```
  [DecimalPlacesConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-decimalplacesconfiguration): 
    DecimalPlacesConfiguration
  [NegativeValueConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-negativevalueconfiguration): 
    NegativeValueConfiguration
  [NullValueFormatConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-nullvalueformatconfiguration): 
    NullValueFormatConfiguration
  [NumberScale](#cfn-quicksight-template-currencydisplayformatconfiguration-numberscale): String
  [Prefix](#cfn-quicksight-template-currencydisplayformatconfiguration-prefix): String
  [SeparatorConfiguration](#cfn-quicksight-template-currencydisplayformatconfiguration-separatorconfiguration): 
    NumericSeparatorConfiguration
  [Suffix](#cfn-quicksight-template-currencydisplayformatconfiguration-suffix): String
  [Symbol](#cfn-quicksight-template-currencydisplayformatconfiguration-symbol): String
```

## Properties<a name="aws-properties-quicksight-template-currencydisplayformatconfiguration-properties"></a>

`DecimalPlacesConfiguration`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-decimalplacesconfiguration"></a>
The option that determines the decimal places configuration\.  
*Required*: No  
*Type*: [DecimalPlacesConfiguration](aws-properties-quicksight-template-decimalplacesconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NegativeValueConfiguration`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-negativevalueconfiguration"></a>
The options that determine the negative value configuration\.  
*Required*: No  
*Type*: [NegativeValueConfiguration](aws-properties-quicksight-template-negativevalueconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullValueFormatConfiguration`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-nullvalueformatconfiguration"></a>
The options that determine the null value format configuration\.  
*Required*: No  
*Type*: [NullValueFormatConfiguration](aws-properties-quicksight-template-nullvalueformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberScale`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-numberscale"></a>
Determines the number scale value for the currency format\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | BILLIONS | MILLIONS | NONE | THOUSANDS | TRILLIONS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-prefix"></a>
Determines the prefix value of the currency format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SeparatorConfiguration`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-separatorconfiguration"></a>
The options that determine the numeric separator configuration\.  
*Required*: No  
*Type*: [NumericSeparatorConfiguration](aws-properties-quicksight-template-numericseparatorconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-suffix"></a>
Determines the suffix value of the currency format\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Symbol`  <a name="cfn-quicksight-template-currencydisplayformatconfiguration-symbol"></a>
Determines the symbol for the currency format\.  
*Required*: No  
*Type*: String  
*Pattern*: `[A-Z]{3}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)