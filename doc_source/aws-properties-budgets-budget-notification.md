# AWS::Budgets::Budget Notification<a name="aws-properties-budgets-budget-notification"></a>

A notification that is associated with a budget\. A budget can have up to ten notifications\. 

Each notification must have at least one subscriber\. A notification can have one SNS subscriber and up to 10 email subscribers, for a total of 11 subscribers\.

For example, if you have a budget for 200 dollars and you want to be notified when you go over 160 dollars, create a notification with the following parameters:
+ A notificationType of `ACTUAL` 
+ A `thresholdType` of `PERCENTAGE` 
+ A `comparisonOperator` of `GREATER_THAN` 
+ A notification `threshold` of `80` 

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
The comparison that is used for this notification\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EQUAL_TO | GREATER_THAN | LESS_THAN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationType`  <a name="cfn-budgets-budget-notification-notificationtype"></a>
Whether the notification is for how much you have spent \(`ACTUAL`\) or for how much you're forecasted to spend \(`FORECASTED`\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ACTUAL | FORECASTED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Threshold`  <a name="cfn-budgets-budget-notification-threshold"></a>
The threshold that is associated with a notification\. Thresholds are always a percentage, and many customers find value being alerted between 50% \- 200% of the budgeted amount\. The maximum limit for your threshold is 1,000,000% above the budgeted amount\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThresholdType`  <a name="cfn-budgets-budget-notification-thresholdtype"></a>
The type of threshold for a notification\. For `ABSOLUTE_VALUE` thresholds, AWS notifies you when you go over or are forecasted to go over your total cost threshold\. For `PERCENTAGE` thresholds, AWS notifies you when you go over or are forecasted to go over a certain percentage of your forecasted spend\. For example, if you have a budget for 200 dollars and you have a `PERCENTAGE` threshold of 80%, AWS notifies you when you go over 160 dollars\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ABSOLUTE_VALUE | PERCENTAGE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-budgets-budget-notification--seealso"></a>
+  [Notification](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Notification.html) in the *AWS Cost Explorer Service Cost Management APIs* 

