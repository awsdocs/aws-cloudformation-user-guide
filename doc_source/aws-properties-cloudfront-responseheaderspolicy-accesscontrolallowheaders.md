# AWS::CloudFront::ResponseHeadersPolicy AccessControlAllowHeaders<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolallowheaders"></a>

A list of HTTP header names that CloudFront includes as values for the `Access-Control-Allow-Headers` HTTP response header\.

For more information about the `Access-Control-Allow-Headers` HTTP response header, see [Access\-Control\-Allow\-Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Headers) in the MDN Web Docs\.

## Syntax<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolallowheaders-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolallowheaders-syntax.json"></a>

```
{
  "[Items](#cfn-cloudfront-responseheaderspolicy-accesscontrolallowheaders-items)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolallowheaders-syntax.yaml"></a>

```
  [Items](#cfn-cloudfront-responseheaderspolicy-accesscontrolallowheaders-items): 
    - String
```

## Properties<a name="aws-properties-cloudfront-responseheaderspolicy-accesscontrolallowheaders-properties"></a>

`Items`  <a name="cfn-cloudfront-responseheaderspolicy-accesscontrolallowheaders-items"></a>
The list of HTTP header names\. You can specify `*` to allow all headers\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)