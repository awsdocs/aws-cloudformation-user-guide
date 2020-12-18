# AWS::Budgets::Budget NotificationWithSubscribers<a name="aws-properties-budgets-budget-notificationwithsubscribers"></a>

A notification with subscribers\. A notification can have one SNS subscriber and up to 10 email subscribers, for a total of 11 subscribers\.

## Syntax<a name="aws-properties-budgets-budget-notificationwithsubscribers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-notificationwithsubscribers-syntax.json"></a>

```
{
  "[Notification](#cfn-budgets-budget-notificationwithsubscribers-notification)" : Notification,
  "[Subscribers](#cfn-budgets-budget-notificationwithsubscribers-subscribers)" : [ Subscriber, ... ]
}
```

### YAML<a name="aws-properties-budgets-budget-notificationwithsubscribers-syntax.yaml"></a>

```
  [Notification](#cfn-budgets-budget-notificationwithsubscribers-notification): 
    Notification
  [Subscribers](#cfn-budgets-budget-notificationwithsubscribers-subscribers): 
    - Subscriber
```

## Properties<a name="aws-properties-budgets-budget-notificationwithsubscribers-properties"></a>

`Notification`  <a name="cfn-budgets-budget-notificationwithsubscribers-notification"></a>
The notification that is associated with a budget\.  
*Required*: Yes  
*Type*: [Notification](aws-properties-budgets-budget-notification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subscribers`  <a name="cfn-budgets-budget-notificationwithsubscribers-subscribers"></a>
A list of subscribers who are subscribed to this notification\.  
*Required*: Yes  
*Type*: List of [Subscriber](aws-properties-budgets-budget-subscriber.md)  
*Maximum*: `11`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-budgets-budget-notificationwithsubscribers--seealso"></a>
+  [NotificationWithSubscribers](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_NotificationWithSubscribers.html) in the *AWS Cost Explorer Service Cost Management APIs* 

