# AWS::CloudFront::OriginRequestPolicy HeadersConfig<a name="aws-properties-cloudfront-originrequestpolicy-headersconfig"></a>

An object that determines whether any HTTP headers \(and if so, which headers\) are included in requests that CloudFront sends to the origin\.

## Syntax<a name="aws-properties-cloudfront-originrequestpolicy-headersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-originrequestpolicy-headersconfig-syntax.json"></a>

```
{
  "[HeaderBehavior](#cfn-cloudfront-originrequestpolicy-headersconfig-headerbehavior)" : String,
  "[Headers](#cfn-cloudfront-originrequestpolicy-headersconfig-headers)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-originrequestpolicy-headersconfig-syntax.yaml"></a>

```
  [HeaderBehavior](#cfn-cloudfront-originrequestpolicy-headersconfig-headerbehavior): String
  [Headers](#cfn-cloudfront-originrequestpolicy-headersconfig-headers): 
    - String
```

## Properties<a name="aws-properties-cloudfront-originrequestpolicy-headersconfig-properties"></a>

`HeaderBehavior`  <a name="cfn-cloudfront-originrequestpolicy-headersconfig-headerbehavior"></a>
Determines whether any HTTP headers are included in requests that CloudFront sends to the origin\. Valid values are:  
+  `none` – HTTP headers are not included in requests that CloudFront sends to the origin\. Even when this field is set to `none`, any headers that are listed in a `CachePolicy` *are* included in origin requests\.
+  `whitelist` – The HTTP headers that are listed in the `Headers` type are included in requests that CloudFront sends to the origin\.
+  `allViewer` – All HTTP headers in viewer requests are included in requests that CloudFront sends to the origin\.
+  `allViewerAndWhitelistCloudFront` – All HTTP headers in viewer requests and the additional CloudFront headers that are listed in the `Headers` type are included in requests that CloudFront sends to the origin\. The additional headers are added by CloudFront\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `allViewer | allViewerAndWhitelistCloudFront | none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Headers`  <a name="cfn-cloudfront-originrequestpolicy-headersconfig-headers"></a>
Contains a list of HTTP header names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)