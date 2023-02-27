# AWS::CloudFront::ResponseHeadersPolicy XSSProtection<a name="aws-properties-cloudfront-responseheaderspolicy-xssprotection"></a>

Determines whether CloudFront includes the `X-XSS-Protection` HTTP response header and the header's value\.

For more information about the `X-XSS-Protection` HTTP response header, see [X\-XSS\-Protection](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-xssprotection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-xssprotection-syntax.json"></a>

```
{
  "[ModeBlock](#cfn-cloudfront-responseheaderspolicy-xssprotection-modeblock)" : Boolean,
  "[Override](#cfn-cloudfront-responseheaderspolicy-xssprotection-override)" : Boolean,
  "[Protection](#cfn-cloudfront-responseheaderspolicy-xssprotection-protection)" : Boolean,
  "[ReportUri](#cfn-cloudfront-responseheaderspolicy-xssprotection-reporturi)" : String
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-xssprotection-syntax.yaml"></a>

```
  [ModeBlock](#cfn-cloudfront-responseheaderspolicy-xssprotection-modeblock): Boolean
  [Override](#cfn-cloudfront-responseheaderspolicy-xssprotection-override): Boolean
  [Protection](#cfn-cloudfront-responseheaderspolicy-xssprotection-protection): Boolean
  [ReportUri](#cfn-cloudfront-responseheaderspolicy-xssprotection-reporturi): String
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-xssprotection-properties"></a>

`ModeBlock`  <a name="cfn-cloudfront-responseheaderspolicy-xssprotection-modeblock"></a>
A Boolean that determines whether CloudFront includes the `mode=block` directive in the `X-XSS-Protection` header\.  
For more information about this directive, see [X\-XSS\-Protection](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection) in the MDN Web Docs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Override`  <a name="cfn-cloudfront-responseheaderspolicy-xssprotection-override"></a>
A Boolean that determines whether CloudFront overrides the `X-XSS-Protection` HTTP response header received from the origin with the one specified in this response headers policy\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protection`  <a name="cfn-cloudfront-responseheaderspolicy-xssprotection-protection"></a>
A Boolean that determines the value of the `X-XSS-Protection` HTTP response header\. When this setting is `true`, the value of the `X-XSS-Protection` header is `1`\. When this setting is `false`, the value of the `X-XSS-Protection` header is `0`\.  
For more information about these settings, see [X\-XSS\-Protection](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection) in the MDN Web Docs\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportUri`  <a name="cfn-cloudfront-responseheaderspolicy-xssprotection-reporturi"></a>
A reporting URI, which CloudFront uses as the value of the `report` directive in the `X-XSS-Protection` header\.  
You cannot specify a `ReportUri` when `ModeBlock` is `true`\.  
For more information about using a reporting URL, see [X\-XSS\-Protection](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection) in the MDN Web Docs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)