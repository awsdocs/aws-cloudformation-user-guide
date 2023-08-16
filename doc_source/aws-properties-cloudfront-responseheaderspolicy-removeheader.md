# AWS::CloudFront::ResponseHeadersPolicy RemoveHeader<a name="aws-properties-cloudfront-responseheaderspolicy-removeheader"></a>

The name of an HTTP header that CloudFront removes from HTTP responses to requests that match the cache behavior that this response headers policy is attached to\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-removeheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-removeheader-syntax.json"></a>

```
{
  "[Header](#cfn-cloudfront-responseheaderspolicy-removeheader-header)" : String
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-removeheader-syntax.yaml"></a>

```
  [Header](#cfn-cloudfront-responseheaderspolicy-removeheader-header): String
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-removeheader-properties"></a>

`Header`  <a name="cfn-cloudfront-responseheaderspolicy-removeheader-header"></a>
The HTTP header name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)