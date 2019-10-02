# AWS::Budgets::Budget Spend<a name="aws-properties-budgets-budget-spend"></a>

The amount of cost or usage that is measured for a budget\.

For example, a `Spend` for `3 GB` of S3 usage would have the following parameters:
+ An `Amount` of `3` 
+ A `unit` of `GB` 

## Syntax<a name="aws-properties-budgets-budget-spend-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-spend-syntax.json"></a>

```
{
  "[Amount](#cfn-budgets-budget-spend-amount)" : Double,
  "[Unit](#cfn-budgets-budget-spend-unit)" : String
}
```

### YAML<a name="aws-properties-budgets-budget-spend-syntax.yaml"></a>

```
  [Amount](#cfn-budgets-budget-spend-amount): Double
  [Unit](#cfn-budgets-budget-spend-unit): String
```

## Properties<a name="aws-properties-budgets-budget-spend-properties"></a>

`Amount`  <a name="cfn-budgets-budget-spend-amount"></a>
The cost or usage amount that is associated with a budget forecast, actual spend, or budget threshold\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-budgets-budget-spend-unit"></a>
The unit of measurement that is used for the budget forecast, actual spend, or budget threshold, such as dollars or GB\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-budgets-budget-spend--seealso"></a>
+  [Spend](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Spend.html) in the *AWS Cost Explorer Service Cost Management APIs* 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
