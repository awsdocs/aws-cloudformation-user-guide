# AWS Billing and Cost Management Budget TimePeriod<a name="aws-properties-budgets-budget-timeperiod"></a>

<a name="aws-properties-budgets-budget-timeperiod-description"></a>The `TimePeriod` property type specifies the period of time covered by a Billing and Cost Management budget\.

<a name="aws-properties-budgets-budget-timeperiod-inheritance"></a> `TimePeriod` is a property of the [AWS Billing and Cost Management Budget BudgetData](aws-properties-budgets-budget-budgetdata.md) property type\.

## Syntax<a name="aws-properties-budgets-budget-timeperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-timeperiod-syntax.json"></a>

```
{
  "[Start](#cfn-budgets-budget-timeperiod-start)" : String,
  "[End](#cfn-budgets-budget-timeperiod-end)" : String
}
```

### YAML<a name="aws-properties-budgets-budget-timeperiod-syntax.yaml"></a>

```
[Start](#cfn-budgets-budget-timeperiod-start): String
[End](#cfn-budgets-budget-timeperiod-end): String
```

## Properties<a name="aws-properties-budgets-budget-timeperiod-properties"></a>

`Start`  <a name="cfn-budgets-budget-timeperiod-start"></a>
The start date for a budget\. If you create your budget and don't specify a start date, AWS defaults to the start of your chosen time period \(i\.e\. DAILY, MONTHLY, QUARTERLY, ANNUALLY\)\. For example, if you create your budget on January 24th 2018, choose `DAILY`, and don't set a start date, AWS sets your start date to `01/24/18 00:00 UTC`\. If you choose `MONTHLY`, AWS sets your start date to `01/01/18 00:00 UTC`\. The defaults are the same for the AWS Billing and Cost Management console and the API\.  
You can change your start date with the `UpdateBudget` API operation\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`End`  <a name="cfn-budgets-budget-timeperiod-end"></a>
The end date for a budget\. If you don't specify an end date, AWS sets your end date to `06/15/2087 00:00 UTC`\. The defaults are the same for the AWS Billing and Cost Management console and the API\.  
After the end date, AWS deletes the budget and all associated notifications and subscribers\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-budgets-budget-timeperiod-seealso"></a>
+ [TimePeriod](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Budget.html#awscostmanagement-Type-budgets_Budget-TimePeriod) in the [AWS Billing and Cost Management API Reference](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/Welcome.html)\. 