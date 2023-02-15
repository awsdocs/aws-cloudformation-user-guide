# AWS::Budgets::Budget Spend<a name="aws-properties-budgets-budget-spend"></a>

The amount of cost or usage that's measured for a budget\.

For example, a `Spend` for `3 GB` of S3 usage has the following parameters:
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
The cost or usage amount that's associated with a budget forecast, actual spend, or budget threshold\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-budgets-budget-spend-unit"></a>
The unit of measurement that's used for the budget forecast, actual spend, or budget threshold, such as USD or GBP\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-budgets-budget-spend--seealso"></a>
+  [Spend](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Spend.html) in the *AWS Cost Explorer Service Cost Management APIs* 

