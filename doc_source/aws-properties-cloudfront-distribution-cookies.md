# AWS::CloudFront::Distribution Cookies<a name="aws-properties-cloudfront-distribution-cookies"></a>

This field is deprecated\. We recommend that you use a cache policy or an origin request policy instead of this field\.

If you want to include cookies in the cache key, use a cache policy\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) in the *Amazon CloudFront Developer Guide*\.

If you want to send cookies to the origin but not include them in the cache key, use an origin request policy\. For more information, see [Creating origin request policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-origin-requests.html#origin-request-create-origin-request-policy) in the *Amazon CloudFront Developer Guide*\.

A complex type that specifies whether you want CloudFront to forward cookies to the origin and, if so, which ones\. For more information about forwarding cookies to the origin, see [How CloudFront Forwards, Caches, and Logs Cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Cookies.html) in the *Amazon CloudFront Developer Guide*\.

## Syntax<a name="aws-properties-cloudfront-distribution-cookies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-cloudfront-distribution-cookies-properties"></a>

`Forward`  <a name="cfn-cloudfront-distribution-cookies-forward"></a>
This field is deprecated\. We recommend that you use a cache policy or an origin request policy instead of this field\.  
If you want to include cookies in the cache key, use a cache policy\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) in the *Amazon CloudFront Developer Guide*\.  
If you want to send cookies to the origin but not include them in the cache key, use origin request policy\. For more information, see [Creating origin request policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-origin-requests.html#origin-request-create-origin-request-policy) in the *Amazon CloudFront Developer Guide*\.  
Specifies which cookies to forward to the origin for this cache behavior: all, none, or the list of cookies specified in the `WhitelistedNames` complex type\.  
Amazon S3 doesn't process cookies\. When the cache behavior is forwarding requests to an Amazon S3 origin, specify none for the `Forward` element\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `all | none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WhitelistedNames`  <a name="cfn-cloudfront-distribution-cookies-whitelistednames"></a>
This field is deprecated\. We recommend that you use a cache policy or an origin request policy instead of this field\.  
If you want to include cookies in the cache key, use a cache policy\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) in the *Amazon CloudFront Developer Guide*\.  
If you want to send cookies to the origin but not include them in the cache key, use an origin request policy\. For more information, see [Creating origin request policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-origin-requests.html#origin-request-create-origin-request-policy) in the *Amazon CloudFront Developer Guide*\.  
Required if you specify `whitelist` for the value of `Forward`\. A complex type that specifies how many different cookies you want CloudFront to forward to the origin for this cache behavior and, if you want to forward selected cookies, the names of those cookies\.  
If you specify `all` or `none` for the value of `Forward`, omit `WhitelistedNames`\. If you change the value of `Forward` from `whitelist` to `all` or `none` and you don't delete the `WhitelistedNames` element and its child elements, CloudFront deletes them automatically\.  
For the current limit on the number of cookie names that you can whitelist for each cache behavior, see [ CloudFront Limits](https://docs.aws.amazon.com/general/latest/gr/xrefaws_service_limits.html#limits_cloudfront) in the *AWS General Reference*\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-cookies--seealso"></a>
+  [CookiePreference](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CookiePreference.html) in the *Amazon CloudFront API Reference* 

