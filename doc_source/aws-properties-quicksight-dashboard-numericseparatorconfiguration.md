# AWS::QuickSight::Dashboard NumericSeparatorConfiguration<a name="aws-properties-quicksight-dashboard-numericseparatorconfiguration"></a>

The options that determine the numeric separator configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-numericseparatorconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-numericseparatorconfiguration-syntax.json"></a>

```
{
  "[DecimalSeparator](#cfn-quicksight-dashboard-numericseparatorconfiguration-decimalseparator)" : String,
  "[ThousandsSeparator](#cfn-quicksight-dashboard-numericseparatorconfiguration-thousandsseparator)" : ThousandSeparatorOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-numericseparatorconfiguration-syntax.yaml"></a>

```
  [DecimalSeparator](#cfn-quicksight-dashboard-numericseparatorconfiguration-decimalseparator): String
  [ThousandsSeparator](#cfn-quicksight-dashboard-numericseparatorconfiguration-thousandsseparator): 
    ThousandSeparatorOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-numericseparatorconfiguration-properties"></a>

`DecimalSeparator`  <a name="cfn-quicksight-dashboard-numericseparatorconfiguration-decimalseparator"></a>
Determines the decimal separator\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COMMA | DOT | SPACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThousandsSeparator`  <a name="cfn-quicksight-dashboard-numericseparatorconfiguration-thousandsseparator"></a>
The options that determine the thousands separator configuration\.  
*Required*: No  
*Type*: [ThousandSeparatorOptions](aws-properties-quicksight-dashboard-thousandseparatoroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)