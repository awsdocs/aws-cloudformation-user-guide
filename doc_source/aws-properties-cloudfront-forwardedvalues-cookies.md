# CloudFront ForwardedValues Cookies<a name="aws-properties-cloudfront-forwardedvalues-cookies"></a>

`Cookies` is a property of the [CloudFront ForwardedValues](aws-properties-cloudfront-forwardedvalues.md) property that describes which cookies are forwarded to the Amazon CloudFront origin\.

## Syntax<a name="w3ab2c21c14d236b5"></a>

### JSON<a name="aws-properties-cloudfront-forwardedvalues-cookies-syntax.json"></a>

```
{
  "[Forward](#cfn-cloudfront-forwardedvalues-cookies-forward)" : String,
  "[WhitelistedNames](#cfn-cloudfront-forwardedvalues-cookies-whitelistednames)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-forwardedvalues-cookies-syntax.yaml"></a>

```
[Forward](#cfn-cloudfront-forwardedvalues-cookies-forward): String
[WhitelistedNames](#cfn-cloudfront-forwardedvalues-cookies-whitelistednames):
  - String
```

## Properties<a name="w3ab2c21c14d236b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [CookiePreference](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CookiePreference.html) data type in the *Amazon CloudFront API Reference*\.

`Forward`  <a name="cfn-cloudfront-forwardedvalues-cookies-forward"></a>
The cookies to forward to the origin of the cache behavior\. You can specify `none`, `all`, or `whitelist`\.  
*Required: *Yes  
*Type*: String

`WhitelistedNames`  <a name="cfn-cloudfront-forwardedvalues-cookies-whitelistednames"></a>
The names of cookies to forward to the origin for the cache behavior\.  
*Required: *Conditional\. Required if you specified `whitelist` for the `Forward` property\.  
*Type*: List of String values