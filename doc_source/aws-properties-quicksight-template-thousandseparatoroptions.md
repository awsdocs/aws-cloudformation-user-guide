# AWS::QuickSight::Template ThousandSeparatorOptions<a name="aws-properties-quicksight-template-thousandseparatoroptions"></a>

The options that determine the thousands separator configuration\.

## Syntax<a name="aws-properties-quicksight-template-thousandseparatoroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-thousandseparatoroptions-syntax.json"></a>

```
{
  "[Symbol](#cfn-quicksight-template-thousandseparatoroptions-symbol)" : String,
  "[Visibility](#cfn-quicksight-template-thousandseparatoroptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-thousandseparatoroptions-syntax.yaml"></a>

```
  [Symbol](#cfn-quicksight-template-thousandseparatoroptions-symbol): String
  [Visibility](#cfn-quicksight-template-thousandseparatoroptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-thousandseparatoroptions-properties"></a>

`Symbol`  <a name="cfn-quicksight-template-thousandseparatoroptions-symbol"></a>
Determines the thousands separator symbol\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COMMA | DOT | SPACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-thousandseparatoroptions-visibility"></a>
Determines the visibility of the thousands separator\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)