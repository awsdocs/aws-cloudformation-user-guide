# AWS::CloudFront::ResponseHeadersPolicy StrictTransportSecurity<a name="aws-properties-cloudfront-responseheaderspolicy-stricttransportsecurity"></a>

Determines whether CloudFront includes the `Strict-Transport-Security` HTTP response header and the header's value\.

For more information about the `Strict-Transport-Security` HTTP response header, see [Strict\-Transport\-Security](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-stricttransportsecurity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-stricttransportsecurity-syntax.json"></a>

```
{
  "[AccessControlMaxAgeSec](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-accesscontrolmaxagesec)" : Integer,
  "[IncludeSubdomains](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-includesubdomains)" : Boolean,
  "[Override](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-override)" : Boolean,
  "[Preload](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-preload)" : Boolean
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-stricttransportsecurity-syntax.yaml"></a>

```
  [AccessControlMaxAgeSec](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-accesscontrolmaxagesec): Integer
  [IncludeSubdomains](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-includesubdomains): Boolean
  [Override](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-override): Boolean
  [Preload](#cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-preload): Boolean
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-stricttransportsecurity-properties"></a>

`AccessControlMaxAgeSec`  <a name="cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-accesscontrolmaxagesec"></a>
A number that CloudFront uses as the value for the `max-age` directive in the `Strict-Transport-Security` HTTP response header\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeSubdomains`  <a name="cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-includesubdomains"></a>
A Boolean that determines whether CloudFront includes the `includeSubDomains` directive in the `Strict-Transport-Security` HTTP response header\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Override`  <a name="cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-override"></a>
A Boolean that determines whether CloudFront overrides the `Strict-Transport-Security` HTTP response header received from the origin with the one specified in this response headers policy\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Preload`  <a name="cfn-cloudfront-responseheaderspolicy-stricttransportsecurity-preload"></a>
A Boolean that determines whether CloudFront includes the `preload` directive in the `Strict-Transport-Security` HTTP response header\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)