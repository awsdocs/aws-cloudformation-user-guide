# AWS Billing and Cost Management Budget Spend<a name="aws-properties-budgets-budget-spend"></a>

<a name="aws-properties-budgets-budget-spend-description"></a>The `Spend` property type specifies the amount of cost, usage, or RI utilization measured by a Billing and Cost Management budget\.

<a name="aws-properties-budgets-budget-spend-inheritance"></a> `Spend` is a property of the [AWS Billing and Cost Management Budget BudgetData](aws-properties-budgets-budget-budgetdata.md) property type\.

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
The cost or usage amount associated with a budget forecast, actual spend, or budget threshold\.  
 *Required*: Yes  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Unit`  <a name="cfn-budgets-budget-spend-unit"></a>
The unit of measurement used for the budget forecast, actual spend, or budget threshold, such as USD or GB\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-budgets-budget-spend-seealso"></a>
+ [Spend](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Spend.html) in the [AWS Billing and Cost Management API Reference](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/Welcome.html)\. 