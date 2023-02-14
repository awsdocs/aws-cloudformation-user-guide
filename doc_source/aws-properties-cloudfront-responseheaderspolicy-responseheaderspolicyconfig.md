# AWS::CloudFront::ResponseHeadersPolicy ResponseHeadersPolicyConfig<a name="aws-properties-cloudfront-responseheaderspolicy-responseheaderspolicyconfig"></a>

A response headers policy configuration\.

A response headers policy configuration contains metadata about the response headers policy, and configurations for sets of HTTP response headers and their values\. CloudFront adds the headers in the policy to HTTP responses that it sends for requests that match a cache behavior associated with the policy\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-syntax.json"></a>

```
{
  "[Comment](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-comment)" : String,
  "[CorsConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-corsconfig)" : CorsConfig,
  "[CustomHeadersConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-customheadersconfig)" : CustomHeadersConfig,
  "[Name](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-name)" : String,
  "[SecurityHeadersConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-securityheadersconfig)" : SecurityHeadersConfig
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-syntax.yaml"></a>

```
  [Comment](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-comment): String
  [CorsConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-corsconfig): 
    CorsConfig
  [CustomHeadersConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-customheadersconfig): 
    CustomHeadersConfig
  [Name](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-name): String
  [SecurityHeadersConfig](#cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-securityheadersconfig): 
    SecurityHeadersConfig
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-properties"></a>

`Comment`  <a name="cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-comment"></a>
A comment to describe the response headers policy\.  
The comment cannot be longer than 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CorsConfig`  <a name="cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-corsconfig"></a>
A configuration for a set of HTTP response headers that are used for cross\-origin resource sharing \(CORS\)\.  
*Required*: No  
*Type*: [CorsConfig](aws-properties-cloudfront-responseheaderspolicy-corsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomHeadersConfig`  <a name="cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-customheadersconfig"></a>
A configuration for a set of custom HTTP response headers\.  
*Required*: No  
*Type*: [CustomHeadersConfig](aws-properties-cloudfront-responseheaderspolicy-customheadersconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-name"></a>
A name to identify the response headers policy\.  
The name must be unique for response headers policies in this AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityHeadersConfig`  <a name="cfn-cloudfront-responseheaderspolicy-responseheaderspolicyconfig-securityheadersconfig"></a>
A configuration for a set of security\-related HTTP response headers\.  
*Required*: No  
*Type*: [SecurityHeadersConfig](aws-properties-cloudfront-responseheaderspolicy-securityheadersconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)