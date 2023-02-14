# AWS::CloudFront::ResponseHeadersPolicy ContentSecurityPolicy<a name="aws-properties-cloudfront-responseheaderspolicy-contentsecuritypolicy"></a>

The policy directives and their values that CloudFront includes as values for the `Content-Security-Policy` HTTP response header\.

For more information about the `Content-Security-Policy` HTTP response header, see [Content\-Security\-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-contentsecuritypolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-contentsecuritypolicy-syntax.json"></a>

```
{
  "[ContentSecurityPolicy](#cfn-cloudfront-responseheaderspolicy-contentsecuritypolicy-contentsecuritypolicy)" : String,
  "[Override](#cfn-cloudfront-responseheaderspolicy-contentsecuritypolicy-override)" : Boolean
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-contentsecuritypolicy-syntax.yaml"></a>

```
  [ContentSecurityPolicy](#cfn-cloudfront-responseheaderspolicy-contentsecuritypolicy-contentsecuritypolicy): String
  [Override](#cfn-cloudfront-responseheaderspolicy-contentsecuritypolicy-override): Boolean
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-contentsecuritypolicy-properties"></a>

`ContentSecurityPolicy`  <a name="cfn-cloudfront-responseheaderspolicy-contentsecuritypolicy-contentsecuritypolicy"></a>
The policy directives and their values that CloudFront includes as values for the `Content-Security-Policy` HTTP response header\.  
*Required*: Yes  
*Type*: [String](#aws-properties-cloudfront-responseheaderspolicy-contentsecuritypolicy)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Override`  <a name="cfn-cloudfront-responseheaderspolicy-contentsecuritypolicy-override"></a>
A Boolean that determines whether CloudFront overrides the `Content-Security-Policy` HTTP response header received from the origin with the one specified in this response headers policy\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)