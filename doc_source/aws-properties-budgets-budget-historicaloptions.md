# AWS::Budgets::Budget HistoricalOptions<a name="aws-properties-budgets-budget-historicaloptions"></a>

The parameters that define or describe the historical data that your auto\-adjusting budget is based on\.

## Syntax<a name="aws-properties-budgets-budget-historicaloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-historicaloptions-syntax.json"></a>

```
{
  "[BudgetAdjustmentPeriod](#cfn-budgets-budget-historicaloptions-budgetadjustmentperiod)" : Integer
}
```

### YAML<a name="aws-properties-budgets-budget-historicaloptions-syntax.yaml"></a>

```
  [BudgetAdjustmentPeriod](#cfn-budgets-budget-historicaloptions-budgetadjustmentperiod): Integer
```

## Properties<a name="aws-properties-budgets-budget-historicaloptions-properties"></a>

`BudgetAdjustmentPeriod`  <a name="cfn-budgets-budget-historicaloptions-budgetadjustmentperiod"></a>
The number of budget periods included in the moving\-average calculation that determines your auto\-adjusted budget amount\. The maximum value depends on the `TimeUnit` granularity of the budget:  
+ For the `DAILY` granularity, the maximum value is `60`\.
+ For the `MONTHLY` granularity, the maximum value is `12`\.
+ For the `QUARTERLY` granularity, the maximum value is `4`\.
+ For the `ANNUALLY` granularity, the maximum value is `1`\.
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `60`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)