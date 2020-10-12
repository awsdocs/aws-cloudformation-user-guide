# AWS::SNS::Topic Subscription<a name="aws-properties-sns-subscription"></a>

 `Subscription` is an embedded property that describes the subscription endpoints of an Amazon SNS topic\.

**Note**  
For full control over subscription behavior \(for example, delivery policy, filtering, raw message delivery, and cross\-region subscriptions\), use the [AWS::SNS::Subscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sns-subscription.html) resource\.

## Syntax<a name="aws-properties-sns-subscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sns-subscription-syntax.json"></a>

```
{
  "[Endpoint](#cfn-sns-topic-subscription-endpoint)" : String,
  "[Protocol](#cfn-sns-topic-subscription-protocol)" : String
}
```

### YAML<a name="aws-properties-sns-subscription-syntax.yaml"></a>

```
  [Endpoint](#cfn-sns-topic-subscription-endpoint): String
  [Protocol](#cfn-sns-topic-subscription-protocol): String
```

## Properties<a name="aws-properties-sns-subscription-properties"></a>

`Endpoint`  <a name="cfn-sns-topic-subscription-endpoint"></a>
The endpoint that receives notifications from the Amazon SNS topic\. The endpoint value depends on the protocol that you specify\. For more information, see the `Endpoint` parameter of the ` [Subscribe](https://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) ` action in the *Amazon Simple Notification Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-sns-topic-subscription-protocol"></a>
The subscription's protocol\. For more information, see the `Protocol` parameter of the ` [Subscribe](https://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) ` action in the *Amazon Simple Notification Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)