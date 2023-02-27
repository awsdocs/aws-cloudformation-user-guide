# AWS::CloudFront::ResponseHeadersPolicy SecurityHeadersConfig<a name="aws-properties-cloudfront-responseheaderspolicy-securityheadersconfig"></a>

A configuration for a set of security\-related HTTP response headers\. CloudFront adds these headers to HTTP responses that it sends for requests that match a cache behavior associated with this response headers policy\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-securityheadersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-securityheadersconfig-syntax.json"></a>

```
{
  "[ContentSecurityPolicy](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-contentsecuritypolicy)" : ContentSecurityPolicy,
  "[ContentTypeOptions](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-contenttypeoptions)" : ContentTypeOptions,
  "[FrameOptions](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-frameoptions)" : FrameOptions,
  "[ReferrerPolicy](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-referrerpolicy)" : ReferrerPolicy,
  "[StrictTransportSecurity](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-stricttransportsecurity)" : StrictTransportSecurity,
  "[XSSProtection](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-xssprotection)" : XSSProtection
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-securityheadersconfig-syntax.yaml"></a>

```
  [ContentSecurityPolicy](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-contentsecuritypolicy): 
    ContentSecurityPolicy
  [ContentTypeOptions](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-contenttypeoptions): 
    ContentTypeOptions
  [FrameOptions](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-frameoptions): 
    FrameOptions
  [ReferrerPolicy](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-referrerpolicy): 
    ReferrerPolicy
  [StrictTransportSecurity](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-stricttransportsecurity): 
    StrictTransportSecurity
  [XSSProtection](#cfn-cloudfront-responseheaderspolicy-securityheadersconfig-xssprotection): 
    XSSProtection
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-securityheadersconfig-properties"></a>

`ContentSecurityPolicy`  <a name="cfn-cloudfront-responseheaderspolicy-securityheadersconfig-contentsecuritypolicy"></a>
The policy directives and their values that CloudFront includes as values for the `Content-Security-Policy` HTTP response header\.  
For more information about the `Content-Security-Policy` HTTP response header, see [Content\-Security\-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) in the MDN Web Docs\.  
*Required*: No  
*Type*: [ContentSecurityPolicy](aws-properties-cloudfront-responseheaderspolicy-contentsecuritypolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentTypeOptions`  <a name="cfn-cloudfront-responseheaderspolicy-securityheadersconfig-contenttypeoptions"></a>
Determines whether CloudFront includes the `X-Content-Type-Options` HTTP response header with its value set to `nosniff`\.  
For more information about the `X-Content-Type-Options` HTTP response header, see [X\-Content\-Type\-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Content-Type-Options) in the MDN Web Docs\.  
*Required*: No  
*Type*: [ContentTypeOptions](aws-properties-cloudfront-responseheaderspolicy-contenttypeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrameOptions`  <a name="cfn-cloudfront-responseheaderspolicy-securityheadersconfig-frameoptions"></a>
Determines whether CloudFront includes the `X-Frame-Options` HTTP response header and the header's value\.  
For more information about the `X-Frame-Options` HTTP response header, see [X\-Frame\-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options) in the MDN Web Docs\.  
*Required*: No  
*Type*: [FrameOptions](aws-properties-cloudfront-responseheaderspolicy-frameoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferrerPolicy`  <a name="cfn-cloudfront-responseheaderspolicy-securityheadersconfig-referrerpolicy"></a>
Determines whether CloudFront includes the `Referrer-Policy` HTTP response header and the header's value\.  
For more information about the `Referrer-Policy` HTTP response header, see [Referrer\-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy) in the MDN Web Docs\.  
*Required*: No  
*Type*: [ReferrerPolicy](aws-properties-cloudfront-responseheaderspolicy-referrerpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StrictTransportSecurity`  <a name="cfn-cloudfront-responseheaderspolicy-securityheadersconfig-stricttransportsecurity"></a>
Determines whether CloudFront includes the `Strict-Transport-Security` HTTP response header and the header's value\.  
For more information about the `Strict-Transport-Security` HTTP response header, see [Strict\-Transport\-Security](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security) in the MDN Web Docs\.  
*Required*: No  
*Type*: [StrictTransportSecurity](aws-properties-cloudfront-responseheaderspolicy-stricttransportsecurity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XSSProtection`  <a name="cfn-cloudfront-responseheaderspolicy-securityheadersconfig-xssprotection"></a>
Determines whether CloudFront includes the `X-XSS-Protection` HTTP response header and the header's value\.  
For more information about the `X-XSS-Protection` HTTP response header, see [X\-XSS\-Protection](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection) in the MDN Web Docs\.  
*Required*: No  
*Type*: [XSSProtection](aws-properties-cloudfront-responseheaderspolicy-xssprotection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)