# AWS Billing and Cost Management Budget Subscriber<a name="aws-properties-budgets-budget-subscriber"></a>

<a name="aws-properties-budgets-budget-subscriber-description"></a>The `Subscriber` property type specifies who to notify for a Billing and Cost Management budget notification\.

<a name="aws-properties-budgets-budget-subscriber-inheritance"></a> `Subscriber` is a property of the [AWS Billing and Cost Management Budget NotificationWithSubscribers](aws-properties-budgets-budget-notificationwithsubscribers.md) property type\.

## Syntax<a name="aws-properties-budgets-budget-subscriber-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budget-subscriber-syntax.json"></a>

```
{
  "[SubscriptionType](#cfn-budgets-budget-subscriber-subscriptiontype)" : String,
  "[Address](#cfn-budgets-budget-subscriber-address)" : String
}
```

### YAML<a name="aws-properties-budgets-budget-subscriber-syntax.yaml"></a>

```
[SubscriptionType](#cfn-budgets-budget-subscriber-subscriptiontype): String
[Address](#cfn-budgets-budget-subscriber-address): String
```

## Properties<a name="aws-properties-budgets-budget-subscriber-properties"></a>

`SubscriptionType`  <a name="cfn-budgets-budget-subscriber-subscriptiontype"></a>
The type of notification that AWS sends to a subscriber, such as `email` or `SNS`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Address`  <a name="cfn-budgets-budget-subscriber-address"></a>
The address that AWS sends budget notifications to, either an SNS topic or an email\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## See Also<a name="aws-properties-budgets-budget-subscriber-seealso"></a>
+ [Subscriber](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_budgets_Subscriber.html) in the [AWS Billing and Cost Management API Reference](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/Welcome.html)\. 