# AWS::CloudFront::ResponseHeadersPolicy FrameOptions<a name="aws-properties-cloudfront-responseheaderspolicy-frameoptions"></a>

Determines whether CloudFront includes the `X-Frame-Options` HTTP response header and the header's value\.

For more information about the `X-Frame-Options` HTTP response header, see [X\-Frame\-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-frameoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-frameoptions-syntax.json"></a>

```
{
  "[FrameOption](#cfn-cloudfront-responseheaderspolicy-frameoptions-frameoption)" : String,
  "[Override](#cfn-cloudfront-responseheaderspolicy-frameoptions-override)" : Boolean
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-frameoptions-syntax.yaml"></a>

```
  [FrameOption](#cfn-cloudfront-responseheaderspolicy-frameoptions-frameoption): String
  [Override](#cfn-cloudfront-responseheaderspolicy-frameoptions-override): Boolean
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-frameoptions-properties"></a>

`FrameOption`  <a name="cfn-cloudfront-responseheaderspolicy-frameoptions-frameoption"></a>
The value of the `X-Frame-Options` HTTP response header\. Valid values are `DENY` and `SAMEORIGIN`\.  
For more information about these values, see [X\-Frame\-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options) in the MDN Web Docs\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DENY | SAMEORIGIN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Override`  <a name="cfn-cloudfront-responseheaderspolicy-frameoptions-override"></a>
A Boolean that determines whether CloudFront overrides the `X-Frame-Options` HTTP response header received from the origin with the one specified in this response headers policy\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)