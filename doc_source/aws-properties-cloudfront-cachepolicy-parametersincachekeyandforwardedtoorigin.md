# AWS::CloudFront::CachePolicy ParametersInCacheKeyAndForwardedToOrigin<a name="aws-properties-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin"></a>

This object determines the values that CloudFront includes in the cache key\. These values can include HTTP headers, cookies, and URL query strings\. CloudFront uses the cache key to find an object in its cache that it can return to the viewer\.

The headers, cookies, and query strings that are included in the cache key are automatically included in requests that CloudFront sends to the origin\. CloudFront sends a request when it can’t find an object in its cache that matches the request’s cache key\. If you want to send values to the origin but *not* include them in the cache key, use `OriginRequestPolicy`\.

## Syntax<a name="aws-properties-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-syntax.json"></a>

```
{
  "[CookiesConfig](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-cookiesconfig)" : CookiesConfig,
  "[EnableAcceptEncodingBrotli](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-enableacceptencodingbrotli)" : Boolean,
  "[EnableAcceptEncodingGzip](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-enableacceptencodinggzip)" : Boolean,
  "[HeadersConfig](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-headersconfig)" : HeadersConfig,
  "[QueryStringsConfig](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-querystringsconfig)" : QueryStringsConfig
}
```

### YAML<a name="aws-properties-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-syntax.yaml"></a>

```
  [CookiesConfig](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-cookiesconfig): 
    CookiesConfig
  [EnableAcceptEncodingBrotli](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-enableacceptencodingbrotli): Boolean
  [EnableAcceptEncodingGzip](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-enableacceptencodinggzip): Boolean
  [HeadersConfig](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-headersconfig): 
    HeadersConfig
  [QueryStringsConfig](#cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-querystringsconfig): 
    QueryStringsConfig
```

## Properties<a name="aws-properties-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-properties"></a>

`CookiesConfig`  <a name="cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-cookiesconfig"></a>
An object that determines whether any cookies in viewer requests \(and if so, which cookies\) are included in the cache key and automatically included in requests that CloudFront sends to the origin\.  
*Required*: Yes  
*Type*: [CookiesConfig](aws-properties-cloudfront-cachepolicy-cookiesconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableAcceptEncodingBrotli`  <a name="cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-enableacceptencodingbrotli"></a>
A flag that can affect whether the `Accept-Encoding` HTTP header is included in the cache key and included in requests that CloudFront sends to the origin\.  
This field is related to the `EnableAcceptEncodingGzip` field\. If one or both of these fields is `true` *and* the viewer request includes the `Accept-Encoding` header, then CloudFront does the following:  
+ Normalizes the value of the viewer’s `Accept-Encoding` header
+ Includes the normalized header in the cache key
+ Includes the normalized header in the request to the origin, if a request is necessary
For more information, see [Compression support](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-policy-compressed-objects) in the *Amazon CloudFront Developer Guide*\.  
If you set this value to `true`, and this cache behavior also has an origin request policy attached, do not include the `Accept-Encoding` header in the origin request policy\. CloudFront always includes the `Accept-Encoding` header in origin requests when the value of this field is `true`, so including this header in an origin request policy has no effect\.  
If both of these fields are `false`, then CloudFront treats the `Accept-Encoding` header the same as any other HTTP header in the viewer request\. By default, it’s not included in the cache key and it’s not included in origin requests\. In this case, you can manually add `Accept-Encoding` to the headers whitelist like any other HTTP header\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableAcceptEncodingGzip`  <a name="cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-enableacceptencodinggzip"></a>
A flag that can affect whether the `Accept-Encoding` HTTP header is included in the cache key and included in requests that CloudFront sends to the origin\.  
This field is related to the `EnableAcceptEncodingBrotli` field\. If one or both of these fields is `true` *and* the viewer request includes the `Accept-Encoding` header, then CloudFront does the following:  
+ Normalizes the value of the viewer’s `Accept-Encoding` header
+ Includes the normalized header in the cache key
+ Includes the normalized header in the request to the origin, if a request is necessary
For more information, see [Compression support](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-policy-compressed-objects) in the *Amazon CloudFront Developer Guide*\.  
If you set this value to `true`, and this cache behavior also has an origin request policy attached, do not include the `Accept-Encoding` header in the origin request policy\. CloudFront always includes the `Accept-Encoding` header in origin requests when the value of this field is `true`, so including this header in an origin request policy has no effect\.  
If both of these fields are `false`, then CloudFront treats the `Accept-Encoding` header the same as any other HTTP header in the viewer request\. By default, it’s not included in the cache key and it’s not included in origin requests\. In this case, you can manually add `Accept-Encoding` to the headers whitelist like any other HTTP header\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeadersConfig`  <a name="cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-headersconfig"></a>
An object that determines whether any HTTP headers \(and if so, which headers\) are included in the cache key and automatically included in requests that CloudFront sends to the origin\.  
*Required*: Yes  
*Type*: [HeadersConfig](aws-properties-cloudfront-cachepolicy-headersconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringsConfig`  <a name="cfn-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin-querystringsconfig"></a>
An object that determines whether any URL query strings in viewer requests \(and if so, which query strings\) are included in the cache key and automatically included in requests that CloudFront sends to the origin\.  
*Required*: Yes  
*Type*: [QueryStringsConfig](aws-properties-cloudfront-cachepolicy-querystringsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)