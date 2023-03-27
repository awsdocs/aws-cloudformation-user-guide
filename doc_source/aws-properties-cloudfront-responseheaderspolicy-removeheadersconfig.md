# AWS::CloudFront::ResponseHeadersPolicy RemoveHeadersConfig<a name="aws-properties-cloudfront-responseheaderspolicy-removeheadersconfig"></a>

A list of HTTP header names that CloudFront removes from HTTP responses to requests that match the cache behavior that this response headers policy is attached to\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-removeheadersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-removeheadersconfig-syntax.json"></a>

```
{
  "[Items](#cfn-cloudfront-responseheaderspolicy-removeheadersconfig-items)" : [ RemoveHeader, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-removeheadersconfig-syntax.yaml"></a>

```
  [Items](#cfn-cloudfront-responseheaderspolicy-removeheadersconfig-items): 
    - RemoveHeader
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-removeheadersconfig-properties"></a>

`Items`  <a name="cfn-cloudfront-responseheaderspolicy-removeheadersconfig-items"></a>
The list of HTTP header names\.  
*Required*: Yes  
*Type*: List of [RemoveHeader](aws-properties-cloudfront-responseheaderspolicy-removeheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)