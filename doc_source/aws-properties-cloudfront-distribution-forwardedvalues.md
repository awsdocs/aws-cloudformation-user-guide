# CloudFront Distribution ForwardedValues<a name="aws-properties-cloudfront-distribution-forwardedvalues"></a>

`ForwardedValues` is a property of the [DefaultCacheBehavior](aws-properties-cloudfront-distribution-defaultcachebehavior.md) and [CacheBehavior](aws-properties-cloudfront-distribution-cachebehavior.md) properties that indicates whether Amazon CloudFront forwards query strings or cookies\.

## Syntax<a name="w3ab2c21c14d272b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-forwardedvalues-syntax.json"></a>

```
{
  "[Cookies](#cfn-cloudfront-distribution-forwardedvalues-cookies)" : Cookies,
  "[Headers](#cfn-cloudfront-distribution-forwardedvalues-headers)" : [ String, ... ],
  "[QueryString](#cfn-cloudfront-distribution-forwardedvalues-querystring)" : Boolean,
  "[QueryStringCacheKeys](#cfn-cloudfront-distribution-forwardedvalues-querystringcachekeys)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-distribution-forwardedvalues-syntax.yaml"></a>

```
[Cookies](#cfn-cloudfront-distribution-forwardedvalues-cookies):
  Cookies
[Headers](#cfn-cloudfront-distribution-forwardedvalues-headers):
  - String
[QueryString](#cfn-cloudfront-distribution-forwardedvalues-querystring): Boolean
[QueryStringCacheKeys](#cfn-cloudfront-distribution-forwardedvalues-querystringcachekeys):
  - String
```

## Properties<a name="w3ab2c21c14d272b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [ForwardedValues](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ForwardedValues.html) data type in the *Amazon CloudFront API Reference*\.

`Cookies`  <a name="cfn-cloudfront-distribution-forwardedvalues-cookies"></a>
Forwards specified cookies to the origin of the cache behavior\. For more information, see [Configuring CloudFront to Cache Based on Cookies](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Cookies.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: [CloudFront Distribution Cookies](aws-properties-cloudfront-distribution-cookies.md)

`Headers`  <a name="cfn-cloudfront-distribution-forwardedvalues-headers"></a>
Specifies the headers that you want Amazon CloudFront to forward to the origin for this cache behavior \(whitelisted headers\)\. For the headers that you specify, Amazon CloudFront also caches separate versions of a specified object that is based on the header values in viewer requests\.  
For custom origins, if you specify a single asterisk \(\["\*"\]\), all headers are forwarded\. If you don't specify a value, only the default headers are forwarded\. For Amazon S3 origins, you can forward only selected headers; specifying \* is not supported\. For more information, see [Configuring CloudFront to Cache Objects Based on Request Headers](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/header-caching.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of String values

`QueryString`  <a name="cfn-cloudfront-distribution-forwardedvalues-querystring"></a>
Indicates whether you want CloudFront to forward query strings to the origin that is associated with this cache behavior\. If so, specify `true`; if not, specify `false`\. For more information about forwarding query strings, see the `QueryString` parameter for the [ForwardedValues](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ForwardedValues.html) type in the *Amazon CloudFront API Reference*\.  
*Required*: Yes  
*Type*: Boolean

`QueryStringCacheKeys`  <a name="cfn-cloudfront-distribution-forwardedvalues-querystringcachekeys"></a>
If you forward query strings to the origin, specifies the query string parameters that CloudFront uses to determine which content to cache\. For more information, see [Configuring CloudFront to Cache Based on Query String Parameters](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/QueryStringParameters.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of String values