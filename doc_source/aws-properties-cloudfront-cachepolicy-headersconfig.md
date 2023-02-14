# AWS::CloudFront::CachePolicy HeadersConfig<a name="aws-properties-cloudfront-cachepolicy-headersconfig"></a>

An object that determines whether any HTTP headers \(and if so, which headers\) are included in the cache key and automatically included in requests that CloudFront sends to the origin\.

## Syntax<a name="aws-properties-cloudfront-cachepolicy-headersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-cachepolicy-headersconfig-syntax.json"></a>

```
{
  "[HeaderBehavior](#cfn-cloudfront-cachepolicy-headersconfig-headerbehavior)" : String,
  "[Headers](#cfn-cloudfront-cachepolicy-headersconfig-headers)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-cachepolicy-headersconfig-syntax.yaml"></a>

```
  [HeaderBehavior](#cfn-cloudfront-cachepolicy-headersconfig-headerbehavior): String
  [Headers](#cfn-cloudfront-cachepolicy-headersconfig-headers): 
    - String
```

## Properties<a name="aws-properties-cloudfront-cachepolicy-headersconfig-properties"></a>

`HeaderBehavior`  <a name="cfn-cloudfront-cachepolicy-headersconfig-headerbehavior"></a>
Determines whether any HTTP headers are included in the cache key and automatically included in requests that CloudFront sends to the origin\. Valid values are:  
+  `none` – HTTP headers are not included in the cache key and are not automatically included in requests that CloudFront sends to the origin\. Even when this field is set to `none`, any headers that are listed in an `OriginRequestPolicy` *are* included in origin requests\.
+  `whitelist` – The HTTP headers that are listed in the `Headers` type are included in the cache key and are automatically included in requests that CloudFront sends to the origin\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Headers`  <a name="cfn-cloudfront-cachepolicy-headersconfig-headers"></a>
Contains a list of HTTP header names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)