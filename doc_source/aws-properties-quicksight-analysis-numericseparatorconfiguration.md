# AWS::QuickSight::Analysis NumericSeparatorConfiguration<a name="aws-properties-quicksight-analysis-numericseparatorconfiguration"></a>

The options that determine the numeric separator configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-numericseparatorconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-numericseparatorconfiguration-syntax.json"></a>

```
{
  "[DecimalSeparator](#cfn-quicksight-analysis-numericseparatorconfiguration-decimalseparator)" : String,
  "[ThousandsSeparator](#cfn-quicksight-analysis-numericseparatorconfiguration-thousandsseparator)" : ThousandSeparatorOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-numericseparatorconfiguration-syntax.yaml"></a>

```
  [DecimalSeparator](#cfn-quicksight-analysis-numericseparatorconfiguration-decimalseparator): String
  [ThousandsSeparator](#cfn-quicksight-analysis-numericseparatorconfiguration-thousandsseparator): 
    ThousandSeparatorOptions
```

## Properties<a name="aws-properties-quicksight-analysis-numericseparatorconfiguration-properties"></a>

`DecimalSeparator`  <a name="cfn-quicksight-analysis-numericseparatorconfiguration-decimalseparator"></a>
Determines the decimal separator\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COMMA | DOT | SPACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThousandsSeparator`  <a name="cfn-quicksight-analysis-numericseparatorconfiguration-thousandsseparator"></a>
The options that determine the thousands separator configuration\.  
*Required*: No  
*Type*: [ThousandSeparatorOptions](aws-properties-quicksight-analysis-thousandseparatoroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)