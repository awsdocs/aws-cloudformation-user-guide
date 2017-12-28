# CloudFront ForwardedValues<a name="aws-properties-cloudfront-forwardedvalues"></a>

`ForwardedValues` is a property of the DefaultCacheBehavior and CacheBehavior properties that indicates whether Amazon CloudFront forwards query strings or cookies\.

## Syntax<a name="w3ab2c21c14d231b5"></a>

### JSON<a name="aws-properties-cloudfront-forwardedvalues-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-cookies)" : Cookies,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-headers)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-querystring)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-querystringcachekeys)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-forwardedvalues-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-cookies):
  Cookies
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-headers):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-querystring): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-forwardedvalues-querystringcachekeys):
  - String
```

## Properties<a name="w3ab2c21c14d231b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [ForwardedValues](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ForwardedValues.html) data type in the *Amazon CloudFront API Reference*\.

`Cookies`  
Forwards specified cookies to the origin of the cache behavior\. For more information, see [Configuring CloudFront to Cache Based on Cookies](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Cookies.html) in the *Amazon CloudFront Developer Guide*\.  
*Required: *No  
*Type*: [CloudFront ForwardedValues Cookies](aws-properties-cloudfront-forwardedvalues-cookies.md)

`Headers`  
Specifies the headers that you want Amazon CloudFront to forward to the origin for this cache behavior \(whitelisted headers\)\. For the headers that you specify, Amazon CloudFront also caches separate versions of a specified object that is based on the header values in viewer requests\.  
For custom origins, if you specify a single asterisk \(\["\*"\]\), all headers are forwarded\. If you don't specify a value, only the default headers are forwarded\. For Amazon S3 origins, you can forward only selected headers; specifying \* is not supported\. For more information, see [Configuring CloudFront to Cache Objects Based on Request Headers](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/header-caching.html) in the *Amazon CloudFront Developer Guide*\.  
*Required: *No  
*Type*: List of String values

`QueryString`  
Indicates whether you want CloudFront to forward query strings to the origin that is associated with this cache behavior\. If so, specify `true`; if not, specify `false`\. For more information about forwarding query strings, see the `QueryString` parameter for the [ForwardedValues](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ForwardedValues.html) type in the *Amazon CloudFront API Reference*\.  
*Required: *Yes  
*Type*: Boolean

`QueryStringCacheKeys`  
If you forward query strings to the origin, specifies the query string parameters that CloudFront uses to determine which content to cache\. For more information, see [Configuring CloudFront to Cache Based on Query String Parameters](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/QueryStringParameters.html) in the *Amazon CloudFront Developer Guide*\.  
*Required: *No  
*Type*: List of String values