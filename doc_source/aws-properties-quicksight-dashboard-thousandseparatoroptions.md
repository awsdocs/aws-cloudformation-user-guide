# AWS::QuickSight::Dashboard ThousandSeparatorOptions<a name="aws-properties-quicksight-dashboard-thousandseparatoroptions"></a>

The options that determine the thousands separator configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-thousandseparatoroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-thousandseparatoroptions-syntax.json"></a>

```
{
  "[Symbol](#cfn-quicksight-dashboard-thousandseparatoroptions-symbol)" : String,
  "[Visibility](#cfn-quicksight-dashboard-thousandseparatoroptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-thousandseparatoroptions-syntax.yaml"></a>

```
  [Symbol](#cfn-quicksight-dashboard-thousandseparatoroptions-symbol): String
  [Visibility](#cfn-quicksight-dashboard-thousandseparatoroptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-thousandseparatoroptions-properties"></a>

`Symbol`  <a name="cfn-quicksight-dashboard-thousandseparatoroptions-symbol"></a>
Determines the thousands separator symbol\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COMMA | DOT | SPACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-thousandseparatoroptions-visibility"></a>
Determines the visibility of the thousands separator\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)