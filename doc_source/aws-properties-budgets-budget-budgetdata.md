# AWS::Budgets::Budget BudgetData<a name="aws-properties-budgets-budget-budgetdata"></a>

Represents the output of the `CreateBudget` operation\. The content consists of the detailed metadata and data file information, and the current status of the `budget` object\.

This is the ARN pattern for a budget: 

 `arn:aws:budgets::AccountId:budget/budgetName` 

## Syntax<a name="aws-properties-budgets-budget-budgetdata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-budgetdata-syntax.json"></a>

```
{
  "[BudgetLimit](#cfn-budgets-budget-budgetdata-budgetlimit)" : Spend,
  "[BudgetName](#cfn-budgets-budget-budgetdata-budgetname)" : String,
  "[BudgetType](#cfn-budgets-budget-budgetdata-budgettype)" : String,
  "[CostFilters](#cfn-budgets-budget-budgetdata-costfilters)" : Json,
  "[CostTypes](#cfn-budgets-budget-budgetdata-costtypes)" : CostTypes,
  "[PlannedBudgetLimits](#cfn-budgets-budget-budgetdata-plannedbudgetlimits)" : Json,
  "[TimePeriod](#cfn-budgets-budget-budgetdata-timeperiod)" : TimePeriod,
  "[TimeUnit](#cfn-budgets-budget-budgetdata-timeunit)" : String
}
```

### YAML<a name="aws-properties-budgets-budget-budgetdata-syntax.yaml"></a>

```
  [BudgetLimit](#cfn-budgets-budget-budgetdata-budgetlimit): 
    Spend
  [BudgetName](#cfn-budgets-budget-budgetdata-budgetname): String
  [BudgetType](#cfn-budgets-budget-budgetdata-budgettype): String
  [CostFilters](#cfn-budgets-budget-budgetdata-costfilters): Json
  [CostTypes](#cfn-budgets-budget-budgetdata-costtypes): 
    CostTypes
  [PlannedBudgetLimits](#cfn-budgets-budget-budgetdata-plannedbudgetlimits): Json
  [TimePeriod](#cfn-budgets-budget-budgetdata-timeperiod): 
    TimePeriod
  [TimeUnit](#cfn-budgets-budget-budgetdata-timeunit): String
```

## Properties<a name="aws-properties-budgets-budget-budgetdata-properties"></a>

`BudgetLimit`  <a name="cfn-budgets-budget-budgetdata-budgetlimit"></a>
The total amount of cost, usage, RI utilization, RI coverage, Savings Plans utilization, or Savings Plans coverage that you want to track with your budget\.  
 `BudgetLimit` is required for cost or usage budgets, but optional for RI or Savings Plans utilization or coverage budgets\. RI and Savings Plans utilization or coverage budgets default to `100`, which is the only valid value for RI or Savings Plans utilization or coverage budgets\. You can't use `BudgetLimit` with `PlannedBudgetLimits` for `CreateBudget` and `UpdateBudget` actions\.   
*Required*: No  
*Type*: [Spend](aws-properties-budgets-budget-spend.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BudgetName`  <a name="cfn-budgets-budget-budgetdata-budgetname"></a>
The name of a budget\. The value must be unique within an account\. `BudgetName` can't include `:` and `\` characters\. If you don't include value for `BudgetName` in the template, Billing and Cost Management assigns your budget a randomly generated name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BudgetType`  <a name="cfn-budgets-budget-budgetdata-budgettype"></a>
Whether this budget tracks costs, usage, RI utilization, RI coverage, Savings Plans utilization, or Savings Plans coverage\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `COST | RI_COVERAGE | RI_UTILIZATION | SAVINGS_PLANS_COVERAGE | SAVINGS_PLANS_UTILIZATION | USAGE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CostFilters`  <a name="cfn-budgets-budget-budgetdata-costfilters"></a>
The cost filters, such as service or tag, that are applied to a budget\.  
AWS Budgets supports the following services as a filter for RI budgets:  
+ Amazon Elastic Compute Cloud \- Compute
+ Amazon Redshift
+ Amazon Relational Database Service
+ Amazon ElastiCache
+ Amazon Elasticsearch Service
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CostTypes`  <a name="cfn-budgets-budget-budgetdata-costtypes"></a>
The types of costs that are included in this `COST` budget\.  
 `USAGE`, `RI_UTILIZATION`, `RI_COVERAGE`, `SAVINGS_PLANS_UTILIZATION`, and `SAVINGS_PLANS_COVERAGE` budgets do not have `CostTypes`\.  
*Required*: No  
*Type*: [CostTypes](aws-properties-budgets-budget-costtypes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlannedBudgetLimits`  <a name="cfn-budgets-budget-budgetdata-plannedbudgetlimits"></a>
A map containing multiple `BudgetLimit`, including current or future limits\.  
 `PlannedBudgetLimits` is available for cost or usage budget and supports monthly and quarterly `TimeUnit`\.   
For monthly budgets, provide 12 months of `PlannedBudgetLimits` values\. This must start from the current month and include the next 11 months\. The `key` is the start of the month, `UTC` in epoch seconds\.   
For quarterly budgets, provide 4 quarters of `PlannedBudgetLimits` value entries in standard calendar quarter increments\. This must start from the current quarter and include the next 3 quarters\. The `key` is the start of the quarter, `UTC` in epoch seconds\.   
If the planned budget expires before 12 months for monthly or 4 quarters for quarterly, provide the `PlannedBudgetLimits` values only for the remaining periods\.  
If the budget begins at a date in the future, provide `PlannedBudgetLimits` values from the start date of the budget\.   
After all of the `BudgetLimit` values in `PlannedBudgetLimits` are used, the budget continues to use the last limit as the `BudgetLimit`\. At that point, the planned budget provides the same experience as a fixed budget\.   
 `DescribeBudget` and `DescribeBudgets` response along with `PlannedBudgetLimits` will also contain `BudgetLimit` representing the current month or quarter limit present in `PlannedBudgetLimits`\. This only applies to budgets created with `PlannedBudgetLimits`\. Budgets created without `PlannedBudgetLimits` will only contain `BudgetLimit`, and no `PlannedBudgetLimits`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimePeriod`  <a name="cfn-budgets-budget-budgetdata-timeperiod"></a>
The period of time that is covered by a budget\. The period has a start date and an end date\. The start date must come before the end date\. There are no restrictions on the end date\.   
The start date for a budget\. If you created your budget and didn't specify a start date, the start date defaults to the start of the chosen time period \(MONTHLY, QUARTERLY, or ANNUALLY\)\. For example, if you create your budget on January 24, 2019, choose `MONTHLY`, and don't set a start date, the start date defaults to `01/01/19 00:00 UTC`\. The defaults are the same for the AWS Billing and Cost Management console and the API\.  
You can change your start date with the `UpdateBudget` operation\.  
After the end date, AWS deletes the budget and all associated notifications and subscribers\.  
*Required*: No  
*Type*: [TimePeriod](aws-properties-budgets-budget-timeperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeUnit`  <a name="cfn-budgets-budget-budgetdata-timeunit"></a>
The length of time until a budget resets the actual and forecasted spend\. `DAILY` is available only for `RI_UTILIZATION` and `RI_COVERAGE` budgets\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ANNUALLY | DAILY | MONTHLY | QUARTERLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-budgets-budget-budgetdata--seealso"></a>
+  [Budget](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_budget.html) in the *AWS Cost Explorer Service Cost Management APIs* 

