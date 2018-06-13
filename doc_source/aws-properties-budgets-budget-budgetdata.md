# AWS Billing and Cost Management Budget BudgetData<a name="aws-properties-budgets-budget-budgetdata"></a>

<a name="aws-properties-budgets-budget-budgetdata-description"></a>The `BudgetData` property type specifies all of the parameters that CloudFront uses to create the budget\. These parameters include the time period that the budget covers, the amount that the budget is for, the name of the budget, what costs, usage, or RI utilization the Billing and Cost Management budget is for, and whether the budget tracks what you have spent or what you are forecast to spend\.

<a name="aws-properties-budgets-budget-budgetdata-inheritance"></a> `BudgetData` is a property of the [AWS::Budgets::Budget](aws-resource-budgets-budget.md) resource\.

## Syntax<a name="aws-properties-budgets-budget-budgetdata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-budgetdata-syntax.json"></a>

```
{
  "[BudgetLimit](#cfn-budgets-budget-budgetdata-budgetlimit)" : [*Spend*](aws-properties-budgets-budget-spend.md),
  "[TimePeriod](#cfn-budgets-budget-budgetdata-timeperiod)" : [*TimePeriod*](aws-properties-budgets-budget-timeperiod.md),
  "[TimeUnit](#cfn-budgets-budget-budgetdata-timeunit)" : String,
  "[CostFilters](#cfn-budgets-budget-budgetdata-costfilters)" : Json,
  "[BudgetName](#cfn-budgets-budget-budgetdata-budgetname)" : String,
  "[CostTypes](#cfn-budgets-budget-budgetdata-costtypes)" : [*CostTypes*](aws-properties-budgets-budget-costtypes.md),
  "[BudgetType](#cfn-budgets-budget-budgetdata-budgettype)" : String
}
```

### YAML<a name="aws-properties-budgets-budget-budgetdata-syntax.yaml"></a>

```
[BudgetLimit](#cfn-budgets-budget-budgetdata-budgetlimit): [*Spend*](aws-properties-budgets-budget-spend.md)
[TimePeriod](#cfn-budgets-budget-budgetdata-timeperiod): [*TimePeriod*](aws-properties-budgets-budget-timeperiod.md)
[TimeUnit](#cfn-budgets-budget-budgetdata-timeunit): String
[CostFilters](#cfn-budgets-budget-budgetdata-costfilters): Json
[BudgetName](#cfn-budgets-budget-budgetdata-budgetname): String
[CostTypes](#cfn-budgets-budget-budgetdata-costtypes): [*CostTypes*](aws-properties-budgets-budget-costtypes.md)
[BudgetType](#cfn-budgets-budget-budgetdata-budgettype): String
```

## Properties<a name="aws-properties-budgets-budget-budgetdata-properties"></a>

`BudgetLimit`  <a name="cfn-budgets-budget-budgetdata-budgetlimit"></a>
The total amount of cost, usage, or RI utilization that you want to track with your budget\.   
The BudgetLimit is required for cost or usage budgets, but optional for RI utilization budgets\. RI utilization budgets default to the only valid value for RI utilization budgets, which is `100`\.   
 *Required*: No  
 *Type*: [Billing and Cost Management Budget Spend](aws-properties-budgets-budget-spend.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TimePeriod`  <a name="cfn-budgets-budget-budgetdata-timeperiod"></a>
The period of time covered by a budget\. Has a start date and an end date\. The start date must come before the end date\. There are no restrictions on the end date\.   
If you create your budget and don't specify a start date, AWS defaults to the start of your chosen time period \(i\.e\. DAILY, MONTHLY, QUARTERLY, ANNUALLY\)\. For example, if you create your budget on January 24th 2018, choose `DAILY`, and don't set a start date, AWS sets your start date to `01/24/18 00:00 UTC`\. If you choose `MONTHLY`, AWS sets your start date to `01/01/18 00:00 UTC`\. If you don't specify an end date, AWS sets your end date to `06/15/87 00:00 UTC`\.  
After the end date, AWS deletes the budget and all associated notifications and subscribers\.  
 *Required*: No  
 *Type*: [Billing and Cost Management Budget TimePeriod](aws-properties-budgets-budget-timeperiod.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TimeUnit`  <a name="cfn-budgets-budget-budgetdata-timeunit"></a>
The length of time until a budget resets the actual and forecasted spend to zero\.  
Valid values are: `DAILY`, `MONTHLY`, `QUARTERLY`, and `ANNUALLY`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CostFilters`  <a name="cfn-budgets-budget-budgetdata-costfilters"></a>
The cost filters applied to a budget, such as service or region\.  
 *Required*: No  
 *Type*: Json  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`BudgetName`  <a name="cfn-budgets-budget-budgetdata-budgetname"></a>
The name of a budget\. Unique within accounts\. `:` and `\` characters are not allowed in the `BudgetName`\. If you do not include a `BudgetName` in the template, Billing and Cost Management assigns your budget a randomly generated name\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CostTypes`  <a name="cfn-budgets-budget-budgetdata-costtypes"></a>
The types of costs included in this budget, such as credits, subscriptions, or taxes\.  
 *Required*: No  
 *Type*: [Billing and Cost Management Budget CostTypes](aws-properties-budgets-budget-costtypes.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`BudgetType`  <a name="cfn-budgets-budget-budgetdata-budgettype"></a>
Whether this budget tracks monetary costs, usage, or RI utilization\.  
Valid values are `USAGE`, `COST`, `RI_UTILIZATION`, and `RI_COVERAGE`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-budgets-budget-budgetdata-seealso"></a>
+ [Budget](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Budget.html) in the [AWS Billing and Cost Management API Reference](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/Welcome.html)\. 