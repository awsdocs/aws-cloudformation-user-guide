# AWS::CloudFront::ResponseHeadersPolicy AccessControlExposeHeaders<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolexposeheaders"></a>

A list of HTTP headers that CloudFront includes as values for the `Access-Control-Expose-Headers` HTTP response header\.

For more information about the `Access-Control-Expose-Headers` HTTP response header, see [Access\-Control\-Expose\-Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Expose-Headers) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolexposeheaders-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolexposeheaders-syntax.json"></a>

```
{
  "[Items](#cfn-cloudfront-responseheaderspolicy-accesscontrolexposeheaders-items)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolexposeheaders-syntax.yaml"></a>

```
  [Items](#cfn-cloudfront-responseheaderspolicy-accesscontrolexposeheaders-items): 
    - String
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolexposeheaders-properties"></a>

`Items`  <a name="cfn-cloudfront-responseheaderspolicy-accesscontrolexposeheaders-items"></a>
The list of HTTP headers\. You can specify `*` to expose all headers\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)