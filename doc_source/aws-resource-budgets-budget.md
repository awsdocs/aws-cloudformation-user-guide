# AWS::Budgets::Budget<a name="aws-resource-budgets-budget"></a>

The `AWS::Budgets::Budget` resource creates, replaces, or deletes budgets for Billing and Cost Management\. For more information, see [Managing Your Costs with Budgets](http://docs.aws.amazon.com/http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/budgets-managing-costs.html) in the [http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/)\. 

**Topics**
+ [Syntax](#aws-resource-budgets-budget-syntax)
+ [Properties](#aws-resource-budgets-budget-properties)
+ [Return Values](#aws-resource-budgets-budget-returnvalues)
+ [Examples](#aws-resource-budgets-budget-examples)
+ [See Also](#aws-resource-budgets-budget-seealso)

## Syntax<a name="aws-resource-budgets-budget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-budgets-budget-syntax.json"></a>

```
{
  "Type" : "AWS::Budgets::Budget",
  "Properties" : {
    "[NotificationsWithSubscribers](#cfn-budgets-budget-notificationswithsubscribers)" : [ [*NotificationWithSubscribers*](aws-properties-budgets-budget-notificationwithsubscribers.md), ... ],
    "[Budget](#cfn-budgets-budget-budget)" : [*BudgetData*](aws-properties-budgets-budget-budgetdata.md)
  }
}
```

### YAML<a name="aws-resource-budgets-budget-syntax.yaml"></a>

```
Type: "AWS::Budgets::Budget"
Properties:
  [NotificationsWithSubscribers](#cfn-budgets-budget-notificationswithsubscribers): 
    - [*NotificationWithSubscribers*](aws-properties-budgets-budget-notificationwithsubscribers.md)
  [Budget](#cfn-budgets-budget-budget): [*BudgetData*](aws-properties-budgets-budget-budgetdata.md)
```

## Properties<a name="aws-resource-budgets-budget-properties"></a>

`NotificationsWithSubscribers`  <a name="cfn-budgets-budget-notificationswithsubscribers"></a>
The notification that you want associated with the budget\. A budget can have up to five notifications, and each notification can have one SNS subscriber and up to ten email subscribers\.  
 *Required*: No  
 *Type*: List of [Billing and Cost Management Budget NotificationWithSubscribers](aws-properties-budgets-budget-notificationwithsubscribers.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Budget`  <a name="cfn-budgets-budget-budget"></a>
The budget for tracking your service usage, costs, and RI utilization\. Single accounts and master and member accounts in an organization can, by default, create budgets\.   
 *Required*: Yes  
 *Type*: [Billing and Cost Management Budget BudgetData](aws-properties-budgets-budget-budgetdata.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-budgets-budget-returnvalues"></a>

### Ref<a name="aws-resource-budgets-budget-ref"></a>

When you pass the logical ID of an `AWS::Budgets::Budget` resource to the intrinsic `Ref` function, the function returns the name of the budget created by the template\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-budgets-budget-examples"></a>

### Budget for 100 USD with two notifications<a name="aws-resource-budgets-budget-example1"></a>

The following example creates a budget for 100 USD amount of costs, with notifications for when you have spent over 80 USD or over 99 USD\. The notifications are sent to the subscribers `email@example.com` and `email2@example.com`\.

#### JSON<a name="aws-resource-budgets-budget-example1.json"></a>

```
    {
        "Description": "Basic Budget test",
        "Resources": {
            "Budget": {
                "Type": "AWS::Budgets::Budget",
                "Properties": {
                    "Budget": {
                        "BudgetLimit": {
                            "Amount": "100",
                            "Unit": "USD"
                        },
                        "TimeUnit": "MONTHLY",
                        "TimePeriod": {
                            "Start": "1225864800",
                            "End": "1926864800"
                        },
                        "BudgetType": "COST",
                        "CostFilters": {
                            "AZ": [
                                "us-east-1",
                                "us-west-1",
                                "us-east-2"
                            ]
                        }
                    },
                    "NotificationsWithSubscribers": [
                        {
                            "Notification": {
                                "NotificationType": "ACTUAL",
                                "ComparisonOperator": "GREATER_THAN",
                                "Threshold": 99
                            },
                            "Subscribers": [
                                {
                                    "SubscriptionType": "EMAIL",
                                    "Address": "email@example.com"
                                },
                                {
                                    "SubscriptionType": "EMAIL",
                                    "Address": "email2@example.com"
                                }
                            ]
                        },
                        {
                            "Notification": {
                                "NotificationType": "ACTUAL",
                                "ComparisonOperator": "GREATER_THAN",
                                "Threshold": 80
                            },
                            "Subscribers": [
                                {
                                    "SubscriptionType": "EMAIL",
                                    "Address": "email@example.com"
                                }
                            ]
                        }
                    ]
                }
            }
        },
        "Outputs": {
            "BudgetId": {
                "Value": "BudgetExample"
            }
        }
    }
```

#### YAML<a name="aws-resource-budgets-budget-example1.yaml"></a>

```
    ---
    Description: "Basic Budget test"
    Resources:
      BudgetExample:
        Type: "AWS::Budgets::Budget"
        Properties:
          Budget:
            BudgetLimit:
              Amount: 100
              Unit: USD
            TimeUnit: MONTHLY
            TimePeriod:
              Start: 1225864800
              End: 1926864800
            BudgetType: COST
            CostFilters:
              AZ:
                - us-east-1
                - us-west-1
                - us-east-2
          NotificationsWithSubscribers:
            - Notification:
                NotificationType: ACTUAL
                ComparisonOperator: GREATER_THAN
                Threshold: 99
              Subscribers:
              - SubscriptionType: EMAIL
                Address: email@example.com
              - SubscriptionType: EMAIL
                Address: email2@example.com
            - Notification:
                NotificationType: ACTUAL
                ComparisonOperator: GREATER_THAN
                Threshold: 80
              Subscribers:
              - SubscriptionType: EMAIL
                Address: email@example.com
    Outputs:
      BudgetId:
        Value: !Ref BudgetExample
```

## See Also<a name="aws-resource-budgets-budget-seealso"></a>
+ [CreateBudget](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_CreateBudget.html) in the [AWS Billing and Cost Management API Reference](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/Welcome.html)\. 