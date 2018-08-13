# AWS::SNS::Subscription<a name="aws-resource-sns-subscription"></a>

The `AWS::SNS::Subscription` resource subscribes an endpoint to an Amazon Simple Notification Service \(Amazon SNS\) topic\. The owner of the endpoint must confirm the subscription before Amazon SNS creates the subscription\.

**Topics**
+ [Syntax](#aws-resource-sns-subscription-syntax)
+ [Properties](#aws-resource-sns-subscription-properties)
+ [Example](#aws-resource-sns-subscription-examples)

## Syntax<a name="aws-resource-sns-subscription-syntax"></a>

### JSON<a name="aws-resource-sns-subscription-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::Subscription",
  "Properties" : {
    "[Endpoint](#cfn-sns-endpoint)" : String,
    "[Protocol](#cfn-sns-protocol)" : String,
    "[TopicArn](#cfn-sns-topicarn)" : String
  }
}
```

### YAML<a name="aws-resource-sns-subscription-syntax.yaml"></a>

```
Type: "AWS::SNS::Subscription"
Properties:
  [Endpoint](#cfn-sns-endpoint): String
  [Protocol](#cfn-sns-protocol): String
  [TopicArn](#cfn-sns-topicarn): String
```

## Properties<a name="aws-resource-sns-subscription-properties"></a>

`Endpoint`  <a name="cfn-sns-endpoint"></a>
The endpoint that receives notifications from the Amazon SNS topic\. The endpoint value depends on the protocol that you specify\. For more information, see the [Subscribe Endpoint](http://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Protocol`  <a name="cfn-sns-protocol"></a>
The subscription's protocol\. For more information, see the [Subscribe Protocol](http://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TopicArn`  <a name="cfn-sns-topicarn"></a>
The Amazon Resource Name \(ARN\) of the topic to subscribe to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Example<a name="aws-resource-sns-subscription-examples"></a>

The following 

### JSON<a name="aws-resource-sns-subscription-example.json"></a>

```
"MySubscription" : {
  "Type" : "AWS::SNS::Subscription",
  "Properties" : {
    "Endpoint" : "test@email.com",
    "Protocol" : "email",
    "TopicArn" : {"Ref" : "MySNSTopic"}
  }
}
```

### YAML<a name="aws-resource-sns-subscription-example.yaml"></a>

```
MySubscription:
  Type: AWS::SNS::Subscription
  Properties:
    Endpoint: test@email.com
    Protocol: email
    TopicArn: !Ref 'MySNSTopic'
```