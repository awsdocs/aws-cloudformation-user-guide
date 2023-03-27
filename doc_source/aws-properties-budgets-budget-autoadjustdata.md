# AWS::Budgets::Budget AutoAdjustData<a name="aws-properties-budgets-budget-autoadjustdata"></a>

The parameters that determine the budget amount for an auto\-adjusting budget\.

## Syntax<a name="aws-properties-budgets-budget-autoadjustdata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-autoadjustdata-syntax.json"></a>

```
{
  "[AutoAdjustType](#cfn-budgets-budget-autoadjustdata-autoadjusttype)" : String,
  "[HistoricalOptions](#cfn-budgets-budget-autoadjustdata-historicaloptions)" : HistoricalOptions
}
```

### YAML<a name="aws-properties-budgets-budget-autoadjustdata-syntax.yaml"></a>

```
  [AutoAdjustType](#cfn-budgets-budget-autoadjustdata-autoadjusttype): String
  [HistoricalOptions](#cfn-budgets-budget-autoadjustdata-historicaloptions): 
    HistoricalOptions
```

## Properties<a name="aws-properties-budgets-budget-autoadjustdata-properties"></a>

`AutoAdjustType`  <a name="cfn-budgets-budget-autoadjustdata-autoadjusttype"></a>
The string that defines whether your budget auto\-adjusts based on historical or forecasted data\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FORECAST | HISTORICAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HistoricalOptions`  <a name="cfn-budgets-budget-autoadjustdata-historicaloptions"></a>
The parameters that define or describe the historical data that your auto\-adjusting budget is based on\.  
*Required*: No  
*Type*: [HistoricalOptions](aws-properties-budgets-budget-historicaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)