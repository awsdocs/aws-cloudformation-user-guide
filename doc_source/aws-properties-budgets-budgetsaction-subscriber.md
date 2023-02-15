# AWS::Budgets::BudgetsAction Subscriber<a name="aws-properties-budgets-budgetsaction-subscriber"></a>

The subscriber to a budget notification\. The subscriber consists of a subscription type and either an Amazon SNS topic or an email address\.

For example, an email subscriber has the following parameters:
+ A `subscriptionType` of `EMAIL` 
+ An `address` of `example@example.com` 

## Syntax<a name="aws-properties-budgets-budgetsaction-subscriber-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budgetsaction-subscriber-syntax.json"></a>

```
{
  "[Address](#cfn-budgets-budgetsaction-subscriber-address)" : String,
  "[Type](#cfn-budgets-budgetsaction-subscriber-type)" : String
}
```

### YAML<a name="aws-properties-budgets-budgetsaction-subscriber-syntax.yaml"></a>

```
  [Address](#cfn-budgets-budgetsaction-subscriber-address): String
  [Type](#cfn-budgets-budgetsaction-subscriber-type): String
```

## Properties<a name="aws-properties-budgets-budgetsaction-subscriber-properties"></a>

`Address`  <a name="cfn-budgets-budgetsaction-subscriber-address"></a>
The address that AWS sends budget notifications to, either an SNS topic or an email\.  
When you create a subscriber, the value of `Address` can't contain line breaks\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-budgets-budgetsaction-subscriber-type"></a>
The type of notification that AWS sends to a subscriber\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)