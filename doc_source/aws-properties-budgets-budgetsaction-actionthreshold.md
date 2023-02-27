# AWS::Budgets::BudgetsAction ActionThreshold<a name="aws-properties-budgets-budgetsaction-actionthreshold"></a>

The trigger threshold of the action\.

## Syntax<a name="aws-properties-budgets-budgetsaction-actionthreshold-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budgetsaction-actionthreshold-syntax.json"></a>

```
{
  "[Type](#cfn-budgets-budgetsaction-actionthreshold-type)" : String,
  "[Value](#cfn-budgets-budgetsaction-actionthreshold-value)" : Double
}
```

### YAML<a name="aws-properties-budgets-budgetsaction-actionthreshold-syntax.yaml"></a>

```
  [Type](#cfn-budgets-budgetsaction-actionthreshold-type): String
  [Value](#cfn-budgets-budgetsaction-actionthreshold-value): Double
```

## Properties<a name="aws-properties-budgets-budgetsaction-actionthreshold-properties"></a>

`Type`  <a name="cfn-budgets-budgetsaction-actionthreshold-type"></a>
The type of threshold for a notification\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ABSOLUTE_VALUE | PERCENTAGE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-budgets-budgetsaction-actionthreshold-value"></a>
The threshold of a notification\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)