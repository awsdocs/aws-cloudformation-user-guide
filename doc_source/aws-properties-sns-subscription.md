# Amazon SNS Subscription Property Type<a name="aws-properties-sns-subscription"></a>

`Subscription` is an embedded property of the `[AWS::SNS::Topic](aws-properties-sns-topic.md)` resource that describes the subscription endpoints for an Amazon Simple Notification Service \(Amazon SNS\) topic\.

## Syntax<a name="w3ab2c21c14e1982b5"></a>

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

## Properties<a name="w3ab2c21c14e1982b7"></a>

`Endpoint`  <a name="cfn-sns-topic-subscription-endpoint"></a>
The subscription's endpoint \(format depends on the protocol\)\. For more information, see the [Subscribe Endpoint](http://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required*: Yes  
*Type*: String

`Protocol`  <a name="cfn-sns-topic-subscription-protocol"></a>
The subscription's protocol\. For more information, see the [Subscribe Protocol](http://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required*: Yes  
*Type*: String