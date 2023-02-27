# AWS::CloudFront::ResponseHeadersPolicy ReferrerPolicy<a name="aws-properties-cloudfront-responseheaderspolicy-referrerpolicy"></a>

Determines whether CloudFront includes the `Referrer-Policy` HTTP response header and the header's value\.

For more information about the `Referrer-Policy` HTTP response header, see [Referrer\-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-referrerpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-referrerpolicy-syntax.json"></a>

```
{
  "[Override](#cfn-cloudfront-responseheaderspolicy-referrerpolicy-override)" : Boolean,
  "[ReferrerPolicy](#cfn-cloudfront-responseheaderspolicy-referrerpolicy-referrerpolicy)" : String
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-referrerpolicy-syntax.yaml"></a>

```
  [Override](#cfn-cloudfront-responseheaderspolicy-referrerpolicy-override): Boolean
  [ReferrerPolicy](#cfn-cloudfront-responseheaderspolicy-referrerpolicy-referrerpolicy): String
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-referrerpolicy-properties"></a>

`Override`  <a name="cfn-cloudfront-responseheaderspolicy-referrerpolicy-override"></a>
A Boolean that determines whether CloudFront overrides the `Referrer-Policy` HTTP response header received from the origin with the one specified in this response headers policy\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferrerPolicy`  <a name="cfn-cloudfront-responseheaderspolicy-referrerpolicy-referrerpolicy"></a>
The value of the `Referrer-Policy` HTTP response header\. Valid values are:  
+  `no-referrer` 
+  `no-referrer-when-downgrade` 
+  `origin` 
+  `origin-when-cross-origin` 
+  `same-origin` 
+  `strict-origin` 
+  `strict-origin-when-cross-origin` 
+  `unsafe-url` 
For more information about these values, see [Referrer\-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy) in the MDN Web Docs\.  
*Required*: Yes  
*Type*: [String](#aws-properties-cloudfront-responseheaderspolicy-referrerpolicy)  
*Allowed values*: `no-referrer | no-referrer-when-downgrade | origin | origin-when-cross-origin | same-origin | strict-origin | strict-origin-when-cross-origin | unsafe-url`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)