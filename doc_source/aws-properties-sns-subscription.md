# Amazon SNS Subscription Property Type<a name="aws-properties-sns-subscription"></a>

`Subscription` is an embedded property of the `AWS::SNS::Topic` resource that describes the subscription endpoints for an Amazon Simple Notification Service \(Amazon SNS\) topic\.

## Syntax<a name="w3ab2c21c14e1620b5"></a>

### JSON<a name="aws-properties-sns-subscription-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topic-subscription-endpoint)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topic-subscription-protocol)" : String
}
```

### YAML<a name="aws-properties-sns-subscription-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topic-subscription-endpoint): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topic-subscription-protocol): String
```

## Properties<a name="w3ab2c21c14e1620b7"></a>

`Endpoint`  
The subscription's endpoint \(format depends on the protocol\)\. For more information, see the [Subscribe Endpoint](http://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required: *Yes  
*Type*: String

`Protocol`  
The subscription's protocol\. For more information, see the [Subscribe Protocol](http://docs.aws.amazon.com/sns/latest/api/API_Subscribe.html) parameter in the *Amazon Simple Notification Service API Reference*\.  
*Required: *Yes  
*Type*: String