# AWS::CloudFront::CachePolicy CookiesConfig<a name="aws-properties-cloudfront-cachepolicy-cookiesconfig"></a>

An object that determines whether any cookies in viewer requests \(and if so, which cookies\) are included in the cache key and automatically included in requests that CloudFront sends to the origin\.

## Syntax<a name="aws-properties-cloudfront-cachepolicy-cookiesconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-cachepolicy-cookiesconfig-syntax.json"></a>

```
{
  "[CookieBehavior](#cfn-cloudfront-cachepolicy-cookiesconfig-cookiebehavior)" : String,
  "[Cookies](#cfn-cloudfront-cachepolicy-cookiesconfig-cookies)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-cachepolicy-cookiesconfig-syntax.yaml"></a>

```
  [CookieBehavior](#cfn-cloudfront-cachepolicy-cookiesconfig-cookiebehavior): String
  [Cookies](#cfn-cloudfront-cachepolicy-cookiesconfig-cookies): 
    - String
```

## Properties<a name="aws-properties-cloudfront-cachepolicy-cookiesconfig-properties"></a>

`CookieBehavior`  <a name="cfn-cloudfront-cachepolicy-cookiesconfig-cookiebehavior"></a>
Determines whether any cookies in viewer requests are included in the cache key and automatically included in requests that CloudFront sends to the origin\. Valid values are:  
+  `none` – Cookies in viewer requests are not included in the cache key and are not automatically included in requests that CloudFront sends to the origin\. Even when this field is set to `none`, any cookies that are listed in an `OriginRequestPolicy` *are* included in origin requests\.
+  `whitelist` – The cookies in viewer requests that are listed in the `CookieNames` type are included in the cache key and automatically included in requests that CloudFront sends to the origin\.
+  `allExcept` – All cookies in viewer requests that are * **not** * listed in the `CookieNames` type are included in the cache key and automatically included in requests that CloudFront sends to the origin\.
+  `all` – All cookies in viewer requests are included in the cache key and are automatically included in requests that CloudFront sends to the origin\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `all | allExcept | none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cookies`  <a name="cfn-cloudfront-cachepolicy-cookiesconfig-cookies"></a>
Contains a list of cookie names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)