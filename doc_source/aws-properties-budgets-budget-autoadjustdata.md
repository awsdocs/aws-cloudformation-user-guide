# AWS::Budgets::Budget AutoAdjustData<a name="aws-properties-budgets-budget-autoadjustdata"></a>

Determine the budget amount for an auto\-adjusting budget\.

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

## Examples<a name="aws-properties-budgets-budget-autoadjustdata--examples"></a>



### Creating an auto\-adjusting AWS budget based on historical data<a name="aws-properties-budgets-budget-autoadjustdata--examples--Creating_an_auto-adjusting__budget_based_on_historical_data"></a>

The following example creates an auto\-adjusting AWS budget based on historical data with a 6 months adjustment period\. The maximum value of the budget adjustment period depends on the `TimeUnit` granularity of the budget\. For example, if you set `TimeUnit` to use the `MONTHLY` value, then the maximum value of `BudgetAdjustmentPeriod` is 12\. For more information, see [BudgetAdjustmentPeriod](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-budgets-budget-historicaloptions.html#cfn-budgets-budget-historicaloptions-budgetadjustmentperiod) in `HistoricalOptions`\.

#### JSON<a name="aws-properties-budgets-budget-autoadjustdata--examples--Creating_an_auto-adjusting__budget_based_on_historical_data--json"></a>

```
{
    "Resources": {
        "BudgetExample": {
            "Type": "AWS::Budgets::Budget",
            "Properties": {
                "Budget": {
                    "BudgetType": "COST",
                    "TimeUnit": "MONTHLY",
                    "AutoAdjustData": {
                        "AutoAdjustType": "HISTORICAL",
                        "HistoricalOptions": {
                            "BudgetAdjustmentPeriod": 6
                        }
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-properties-budgets-budget-autoadjustdata--examples--Creating_an_auto-adjusting__budget_based_on_historical_data--yaml"></a>

```
Resources:
  BudgetExample:
    Type: "AWS::Budgets::Budget"
    Properties:
      Budget:
        BudgetType: COST
        TimeUnit: MONTHLY
        AutoAdjustData:
          AutoAdjustType: HISTORICAL
          HistoricalOptions:
              BudgetAdjustmentPeriod: 6
```