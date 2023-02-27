# AWS::CloudFront::ResponseHeadersPolicy CustomHeader<a name="aws-properties-cloudfront-responseheaderspolicy-customheader"></a>

An HTTP response header name and its value\. CloudFront includes this header in HTTP responses that it sends for requests that match a cache behavior that's associated with this response headers policy\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-customheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-customheader-syntax.json"></a>

```
{
  "[Header](#cfn-cloudfront-responseheaderspolicy-customheader-header)" : String,
  "[Override](#cfn-cloudfront-responseheaderspolicy-customheader-override)" : Boolean,
  "[Value](#cfn-cloudfront-responseheaderspolicy-customheader-value)" : String
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-customheader-syntax.yaml"></a>

```
  [Header](#cfn-cloudfront-responseheaderspolicy-customheader-header): String
  [Override](#cfn-cloudfront-responseheaderspolicy-customheader-override): Boolean
  [Value](#cfn-cloudfront-responseheaderspolicy-customheader-value): String
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-customheader-properties"></a>

`Header`  <a name="cfn-cloudfront-responseheaderspolicy-customheader-header"></a>
The HTTP response header name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Override`  <a name="cfn-cloudfront-responseheaderspolicy-customheader-override"></a>
A Boolean that determines whether CloudFront overrides a response header with the same name received from the origin with the header specified here\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-cloudfront-responseheaderspolicy-customheader-value"></a>
The value for the HTTP response header\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)