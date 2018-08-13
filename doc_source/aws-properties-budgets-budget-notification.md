# AWS Billing and Cost Management Budget Notification<a name="aws-properties-budgets-budget-notification"></a>

<a name="aws-properties-budgets-budget-notification-description"></a>The `Notification` property type specifies who to notify for a Billing and Cost Management budget\.

<a name="aws-properties-budgets-budget-notification-inheritance"></a> `Notification` is a property of the [AWS Billing and Cost Management Budget NotificationWithSubscribers](aws-properties-budgets-budget-notificationwithsubscribers.md) property type\.

## Syntax<a name="aws-properties-budgets-budget-notification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-notification-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-budgets-budget-notification-comparisonoperator)" : String,
  "[NotificationType](#cfn-budgets-budget-notification-notificationtype)" : String,
  "[Threshold](#cfn-budgets-budget-notification-threshold)" : Double,
  "[ThresholdType](#cfn-budgets-budget-notification-thresholdtype)" : String
}
```

### YAML<a name="aws-properties-budgets-budget-notification-syntax.yaml"></a>

```
[ComparisonOperator](#cfn-budgets-budget-notification-comparisonoperator): String
[NotificationType](#cfn-budgets-budget-notification-notificationtype): String
[Threshold](#cfn-budgets-budget-notification-threshold): Double
[ThresholdType](#cfn-budgets-budget-notification-thresholdtype): String
```

## Properties<a name="aws-properties-budgets-budget-notification-properties"></a>

`ComparisonOperator`  <a name="cfn-budgets-budget-notification-comparisonoperator"></a>
The comparison used for this notification\. Valid Values are `GREATER_THAN`, `LESS_THAN`, and `EQUAL_TO`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`NotificationType`  <a name="cfn-budgets-budget-notification-notificationtype"></a>
Whether the notification is for how much you have spent or for how much you are forecasted to spend\. For `ACTUAL` thresholds, AWS notifies you when you go over the threshold, and for `FORECASTED` thresholds AWS notifies you when you are forecasted to go over the threshold\. Valid values are `ACTUAL` and `FORECASTED`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Threshold`  <a name="cfn-budgets-budget-notification-threshold"></a>
The threshold associated with a notification\. The minimum valid value is `0.1`, and the maximum valid value is `1000000000`\.  
 *Required*: Yes  
 *Type*: Double  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ThresholdType`  <a name="cfn-budgets-budget-notification-thresholdtype"></a>
The type of threshold for a notification\. Valid values are `PERCENTAGE ` and `ABSOLUTE_VALUE`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## See Also<a name="aws-properties-budgets-budget-notification-seealso"></a>
+ [Notification](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Notification.html) in the [AWS Billing and Cost Management API Reference](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/Welcome.html)\. 