# AWS::Budgets::Budget TimePeriod<a name="aws-properties-budgets-budget-timeperiod"></a>

The period of time that is covered by a budget\. The period has a start date and an end date\. The start date must come before the end date\. There are no restrictions on the end date\. 

## Syntax<a name="aws-properties-budgets-budget-timeperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-timeperiod-syntax.json"></a>

```
{
  "[End](#cfn-budgets-budget-timeperiod-end)" : String,
  "[Start](#cfn-budgets-budget-timeperiod-start)" : String
}
```

### YAML<a name="aws-properties-budgets-budget-timeperiod-syntax.yaml"></a>

```
  [End](#cfn-budgets-budget-timeperiod-end): String
  [Start](#cfn-budgets-budget-timeperiod-start): String
```

## Properties<a name="aws-properties-budgets-budget-timeperiod-properties"></a>

`End`  <a name="cfn-budgets-budget-timeperiod-end"></a>
The end date for a budget\. If you didn't specify an end date, AWS set your end date to `06/15/87 00:00 UTC`\. The defaults are the same for the AWS Billing and Cost Management console and the API\.  
After the end date, AWS deletes the budget and all associated notifications and subscribers\. You can change your end date with the `UpdateBudget` operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Start`  <a name="cfn-budgets-budget-timeperiod-start"></a>
The start date for a budget\. If you created your budget and didn't specify a start date, the start date defaults to the start of the chosen time period \(MONTHLY, QUARTERLY, or ANNUALLY\)\. For example, if you create your budget on January 24, 2019, choose `MONTHLY`, and don't set a start date, the start date defaults to `01/01/19 00:00 UTC`\. The defaults are the same for the AWS Billing and Cost Management console and the API\.  
You can change your start date with the `UpdateBudget` operation\.  
Valid values depend on the value of `BudgetType`:  
+ If `BudgetType` is `COST` or `USAGE`: Valid values are `MONTHLY`, `QUARTERLY`, and `ANNUALLY`\.
+ If `BudgetType` is `RI_UTILIZATION` or `RI_COVERAGE`: Valid values are `DAILY`, `MONTHLY`, `QUARTERLY`, and `ANNUALLY`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-budgets-budget-timeperiod--seealso"></a>
+  [TimePeriod](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_TimePeriod.html) in the *AWS Cost Explorer Service Cost Management APIs* 

