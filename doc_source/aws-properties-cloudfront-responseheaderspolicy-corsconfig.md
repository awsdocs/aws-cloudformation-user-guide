# AWS::CloudFront::ResponseHeadersPolicy CorsConfig<a name="aws-properties-cloudfront-responseheaderspolicy-corsconfig"></a>

A configuration for a set of HTTP response headers that are used for cross\-origin resource sharing \(CORS\)\. CloudFront adds these headers to HTTP responses that it sends for CORS requests that match a cache behavior associated with this response headers policy\.

For more information about CORS, see [Cross\-Origin Resource Sharing \(CORS\)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-corsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-corsconfig-syntax.json"></a>

```
{
  "[AccessControlAllowCredentials](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowcredentials)" : Boolean,
  "[AccessControlAllowHeaders](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowheaders)" : AccessControlAllowHeaders,
  "[AccessControlAllowMethods](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowmethods)" : AccessControlAllowMethods,
  "[AccessControlAllowOrigins](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolalloworigins)" : AccessControlAllowOrigins,
  "[AccessControlExposeHeaders](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolexposeheaders)" : AccessControlExposeHeaders,
  "[AccessControlMaxAgeSec](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolmaxagesec)" : Integer,
  "[OriginOverride](#cfn-cloudfront-responseheaderspolicy-corsconfig-originoverride)" : Boolean
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-corsconfig-syntax.yaml"></a>

```
  [AccessControlAllowCredentials](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowcredentials): Boolean
  [AccessControlAllowHeaders](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowheaders): 
    AccessControlAllowHeaders
  [AccessControlAllowMethods](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowmethods): 
    AccessControlAllowMethods
  [AccessControlAllowOrigins](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolalloworigins): 
    AccessControlAllowOrigins
  [AccessControlExposeHeaders](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolexposeheaders): 
    AccessControlExposeHeaders
  [AccessControlMaxAgeSec](#cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolmaxagesec): Integer
  [OriginOverride](#cfn-cloudfront-responseheaderspolicy-corsconfig-originoverride): Boolean
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-corsconfig-properties"></a>

`AccessControlAllowCredentials`  <a name="cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowcredentials"></a>
A Boolean that CloudFront uses as the value for the `Access-Control-Allow-Credentials` HTTP response header\.  
For more information about the `Access-Control-Allow-Credentials` HTTP response header, see [Access\-Control\-Allow\-Credentials](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Credentials) in the MDN Web Docs\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessControlAllowHeaders`  <a name="cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowheaders"></a>
A list of HTTP header names that CloudFront includes as values for the `Access-Control-Allow-Headers` HTTP response header\.  
For more information about the `Access-Control-Allow-Headers` HTTP response header, see [Access\-Control\-Allow\-Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Headers) in the MDN Web Docs\.  
*Required*: Yes  
*Type*: [AccessControlAllowHeaders](aws-properties-cloudfront-responseheaderspolicy-accesscontrolallowheaders.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessControlAllowMethods`  <a name="cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolallowmethods"></a>
A list of HTTP methods that CloudFront includes as values for the `Access-Control-Allow-Methods` HTTP response header\.  
For more information about the `Access-Control-Allow-Methods` HTTP response header, see [Access\-Control\-Allow\-Methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Methods) in the MDN Web Docs\.  
*Required*: Yes  
*Type*: [AccessControlAllowMethods](aws-properties-cloudfront-responseheaderspolicy-accesscontrolallowmethods.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessControlAllowOrigins`  <a name="cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolalloworigins"></a>
A list of origins \(domain names\) that CloudFront can use as the value for the `Access-Control-Allow-Origin` HTTP response header\.  
For more information about the `Access-Control-Allow-Origin` HTTP response header, see [Access\-Control\-Allow\-Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin) in the MDN Web Docs\.  
*Required*: Yes  
*Type*: [AccessControlAllowOrigins](aws-properties-cloudfront-responseheaderspolicy-accesscontrolalloworigins.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessControlExposeHeaders`  <a name="cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolexposeheaders"></a>
A list of HTTP headers that CloudFront includes as values for the `Access-Control-Expose-Headers` HTTP response header\.  
For more information about the `Access-Control-Expose-Headers` HTTP response header, see [Access\-Control\-Expose\-Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Expose-Headers) in the MDN Web Docs\.  
*Required*: No  
*Type*: [AccessControlExposeHeaders](aws-properties-cloudfront-responseheaderspolicy-accesscontrolexposeheaders.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessControlMaxAgeSec`  <a name="cfn-cloudfront-responseheaderspolicy-corsconfig-accesscontrolmaxagesec"></a>
A number that CloudFront uses as the value for the `Access-Control-Max-Age` HTTP response header\.  
For more information about the `Access-Control-Max-Age` HTTP response header, see [Access\-Control\-Max\-Age](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Max-Age) in the MDN Web Docs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginOverride`  <a name="cfn-cloudfront-responseheaderspolicy-corsconfig-originoverride"></a>
A Boolean that determines whether CloudFront overrides HTTP response headers received from the origin with the ones specified in this response headers policy\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)