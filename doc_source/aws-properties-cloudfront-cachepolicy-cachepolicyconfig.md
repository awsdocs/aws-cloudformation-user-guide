# AWS::CloudFront::CachePolicy CachePolicyConfig<a name="aws-properties-cloudfront-cachepolicy-cachepolicyconfig"></a>

A cache policy configuration\.

This configuration determines the following:
+ The values that CloudFront includes in the cache key\. These values can include HTTP headers, cookies, and URL query strings\. CloudFront uses the cache key to find an object in its cache that it can return to the viewer\.
+ The default, minimum, and maximum time to live \(TTL\) values that you want objects to stay in the CloudFront cache\.

The headers, cookies, and query strings that are included in the cache key are automatically included in requests that CloudFront sends to the origin\. CloudFront sends a request when it can’t find a valid object in its cache that matches the request’s cache key\. If you want to send values to the origin but *not* include them in the cache key, use `OriginRequestPolicy`\.

## Syntax<a name="aws-properties-cloudfront-cachepolicy-cachepolicyconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-cachepolicy-cachepolicyconfig-syntax.json"></a>

```
{
  "[Comment](#cfn-cloudfront-cachepolicy-cachepolicyconfig-comment)" : String,
  "[DefaultTTL](#cfn-cloudfront-cachepolicy-cachepolicyconfig-defaultttl)" : Double,
  "[MaxTTL](#cfn-cloudfront-cachepolicy-cachepolicyconfig-maxttl)" : Double,
  "[MinTTL](#cfn-cloudfront-cachepolicy-cachepolicyconfig-minttl)" : Double,
  "[Name](#cfn-cloudfront-cachepolicy-cachepolicyconfig-name)" : String,
  "[ParametersInCacheKeyAndForwardedToOrigin](#cfn-cloudfront-cachepolicy-cachepolicyconfig-parametersincachekeyandforwardedtoorigin)" : ParametersInCacheKeyAndForwardedToOrigin
}
```

### YAML<a name="aws-properties-cloudfront-cachepolicy-cachepolicyconfig-syntax.yaml"></a>

```
  [Comment](#cfn-cloudfront-cachepolicy-cachepolicyconfig-comment): String
  [DefaultTTL](#cfn-cloudfront-cachepolicy-cachepolicyconfig-defaultttl): Double
  [MaxTTL](#cfn-cloudfront-cachepolicy-cachepolicyconfig-maxttl): Double
  [MinTTL](#cfn-cloudfront-cachepolicy-cachepolicyconfig-minttl): Double
  [Name](#cfn-cloudfront-cachepolicy-cachepolicyconfig-name): String
  [ParametersInCacheKeyAndForwardedToOrigin](#cfn-cloudfront-cachepolicy-cachepolicyconfig-parametersincachekeyandforwardedtoorigin): 
    ParametersInCacheKeyAndForwardedToOrigin
```

## Properties<a name="aws-properties-cloudfront-cachepolicy-cachepolicyconfig-properties"></a>

`Comment`  <a name="cfn-cloudfront-cachepolicy-cachepolicyconfig-comment"></a>
A comment to describe the cache policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultTTL`  <a name="cfn-cloudfront-cachepolicy-cachepolicyconfig-defaultttl"></a>
The default amount of time, in seconds, that you want objects to stay in the CloudFront cache before CloudFront sends another request to the origin to see if the object has been updated\. CloudFront uses this value as the object’s time to live \(TTL\) only when the origin does *not* send `Cache-Control` or `Expires` headers with the object\. For more information, see [Managing How Long Content Stays in an Edge Cache \(Expiration\)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Expiration.html) in the *Amazon CloudFront Developer Guide*\.  
The default value for this field is 86400 seconds \(one day\)\. If the value of `MinTTL` is more than 86400 seconds, then the default value for this field is the same as the value of `MinTTL`\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxTTL`  <a name="cfn-cloudfront-cachepolicy-cachepolicyconfig-maxttl"></a>
The maximum amount of time, in seconds, that objects stay in the CloudFront cache before CloudFront sends another request to the origin to see if the object has been updated\. CloudFront uses this value only when the origin sends `Cache-Control` or `Expires` headers with the object\. For more information, see [Managing How Long Content Stays in an Edge Cache \(Expiration\)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Expiration.html) in the *Amazon CloudFront Developer Guide*\.  
The default value for this field is 31536000 seconds \(one year\)\. If the value of `MinTTL` or `DefaultTTL` is more than 31536000 seconds, then the default value for this field is the same as the value of `DefaultTTL`\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinTTL`  <a name="cfn-cloudfront-cachepolicy-cachepolicyconfig-minttl"></a>
The minimum amount of time, in seconds, that you want objects to stay in the CloudFront cache before CloudFront sends another request to the origin to see if the object has been updated\. For more information, see [Managing How Long Content Stays in an Edge Cache \(Expiration\)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Expiration.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudfront-cachepolicy-cachepolicyconfig-name"></a>
A unique name to identify the cache policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParametersInCacheKeyAndForwardedToOrigin`  <a name="cfn-cloudfront-cachepolicy-cachepolicyconfig-parametersincachekeyandforwardedtoorigin"></a>
The HTTP headers, cookies, and URL query strings to include in the cache key\. The values included in the cache key are automatically included in requests that CloudFront sends to the origin\.  
*Required*: Yes  
*Type*: [ParametersInCacheKeyAndForwardedToOrigin](aws-properties-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)