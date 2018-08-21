# AWS Billing and Cost Management Budget NotificationWithSubscribers<a name="aws-properties-budgets-budget-notificationwithsubscribers"></a>

<a name="aws-properties-budgets-budget-notificationwithsubscribers-description"></a>The `NotificationWithSubscribers` property type specifies who to notify when a Billing and Cost Management budget passes or is predicted to pass its threshold\.

<a name="aws-properties-budgets-budget-notificationwithsubscribers-inheritance"></a> `NotificationWithSubscribers` is a property of the [AWS::Budgets::Budget](aws-resource-budgets-budget.md) resource\.

## Syntax<a name="aws-properties-budgets-budget-notificationwithsubscribers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-notificationwithsubscribers-syntax.json"></a>

```
{
  "[Subscribers](#cfn-budgets-budget-notificationwithsubscribers-subscribers)" : [ [*Subscriber*](aws-properties-budgets-budget-subscriber.md), ... ],
  "[Notification](#cfn-budgets-budget-notificationwithsubscribers-notification)" : [*Notification*](aws-properties-budgets-budget-notification.md)
}
```

### YAML<a name="aws-properties-budgets-budget-notificationwithsubscribers-syntax.yaml"></a>

```
[Subscribers](#cfn-budgets-budget-notificationwithsubscribers-subscribers): 
  - [*Subscriber*](aws-properties-budgets-budget-subscriber.md)
[Notification](#cfn-budgets-budget-notificationwithsubscribers-notification): [*Notification*](aws-properties-budgets-budget-notification.md)
```

## Properties<a name="aws-properties-budgets-budget-notificationwithsubscribers-properties"></a>

`Subscribers`  <a name="cfn-budgets-budget-notificationwithsubscribers-subscribers"></a>
A list of subscribers who are subscribed to this notification\.  
 *Required*: Yes  
 *Type*: List of [Billing and Cost Management Budget Subscriber](aws-properties-budgets-budget-subscriber.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Notification`  <a name="cfn-budgets-budget-notificationwithsubscribers-notification"></a>
A notification associated with a budget\. A budget can have up to five notifications\.   
Each notification must have at least one subscriber\. A notification can have one SNS subscriber and up to ten email subscribers, for a total of 11 subscribers\.   
For example, if you have a budget for 200 dollars and you want to be notified when you go over 160 dollars, create a notification with the following parameters:  
+ A `thresholdType` of `PERCENTAGE`
+ A `threshold` of `80`
+ A `notificationType` of `ACTUAL`
+ A `comparisonOperator` of `GREATER_THAN`
 *Required*: Yes  
 *Type*: [Billing and Cost Management Budget Notification](aws-properties-budgets-budget-notification.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## See Also<a name="aws-properties-budgets-budget-notificationwithsubscribers-seealso"></a>
+ [NotificationWithSubscribers](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_NotificationWithSubscribers.html) in the [AWS Billing and Cost Management API Reference](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/Welcome.html)\. 