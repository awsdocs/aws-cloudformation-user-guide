# CloudFront Distribution Cookies<a name="aws-properties-cloudfront-distribution-cookies"></a>

`Cookies` is a property of the [CloudFront Distribution ForwardedValues](aws-properties-cloudfront-distribution-forwardedvalues.md) property that describes which cookies are forwarded to the Amazon CloudFront origin\.

## Syntax<a name="w3ab2c21c14d248b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-cookies-syntax.json"></a>

```
{
  "[Forward](#cfn-cloudfront-distribution-cookies-forward)" : String,
  "[WhitelistedNames](#cfn-cloudfront-distribution-cookies-whitelistednames)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-distribution-cookies-syntax.yaml"></a>

```
[Forward](#cfn-cloudfront-distribution-cookies-forward): String
[WhitelistedNames](#cfn-cloudfront-distribution-cookies-whitelistednames):
  - String
```

## Properties<a name="w3ab2c21c14d248b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [CookiePreference](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CookiePreference.html) data type in the *Amazon CloudFront API Reference*\.

`Forward`  <a name="cfn-cloudfront-distribution-cookies-forward"></a>
The cookies to forward to the origin of the cache behavior\. You can specify `none`, `all`, or `whitelist`\.  
*Required*: Yes  
*Type*: String

`WhitelistedNames`  <a name="cfn-cloudfront-distribution-cookies-whitelistednames"></a>
The names of cookies to forward to the origin for the cache behavior\.  
*Required*: Conditional\. Required if you specified `whitelist` for the `Forward` property\.  
*Type*: List of String values