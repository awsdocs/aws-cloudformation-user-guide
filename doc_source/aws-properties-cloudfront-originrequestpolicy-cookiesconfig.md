# AWS::CloudFront::OriginRequestPolicy CookiesConfig<a name="aws-properties-cloudfront-originrequestpolicy-cookiesconfig"></a>

An object that determines whether any cookies in viewer requests \(and if so, which cookies\) are included in requests that CloudFront sends to the origin\.

## Syntax<a name="aws-properties-cloudfront-originrequestpolicy-cookiesconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-originrequestpolicy-cookiesconfig-syntax.json"></a>

```
{
  "[CookieBehavior](#cfn-cloudfront-originrequestpolicy-cookiesconfig-cookiebehavior)" : String,
  "[Cookies](#cfn-cloudfront-originrequestpolicy-cookiesconfig-cookies)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-originrequestpolicy-cookiesconfig-syntax.yaml"></a>

```
  [CookieBehavior](#cfn-cloudfront-originrequestpolicy-cookiesconfig-cookiebehavior): String
  [Cookies](#cfn-cloudfront-originrequestpolicy-cookiesconfig-cookies): 
    - String
```

## Properties<a name="aws-properties-cloudfront-originrequestpolicy-cookiesconfig-properties"></a>

`CookieBehavior`  <a name="cfn-cloudfront-originrequestpolicy-cookiesconfig-cookiebehavior"></a>
Determines whether cookies in viewer requests are included in requests that CloudFront sends to the origin\. Valid values are:  
+  `none` – Cookies in viewer requests are not included in requests that CloudFront sends to the origin\. Even when this field is set to `none`, any cookies that are listed in a `CachePolicy` *are* included in origin requests\.
+  `whitelist` – The cookies in viewer requests that are listed in the `CookieNames` type are included in requests that CloudFront sends to the origin\.
+  `all` – All cookies in viewer requests are included in requests that CloudFront sends to the origin\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `all | none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cookies`  <a name="cfn-cloudfront-originrequestpolicy-cookiesconfig-cookies"></a>
Contains a list of cookie names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)