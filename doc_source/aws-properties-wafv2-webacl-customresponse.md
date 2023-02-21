# AWS::WAFv2::WebACL CustomResponse<a name="aws-properties-wafv2-webacl-customresponse"></a>

A custom response to send to the client\. You can define a custom response for rule actions and default web ACL actions that are set to the block action\. 

For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

## Syntax<a name="aws-properties-wafv2-webacl-customresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-customresponse-syntax.json"></a>

```
{
  "[CustomResponseBodyKey](#cfn-wafv2-webacl-customresponse-customresponsebodykey)" : String,
  "[ResponseCode](#cfn-wafv2-webacl-customresponse-responsecode)" : Integer,
  "[ResponseHeaders](#cfn-wafv2-webacl-customresponse-responseheaders)" : [ CustomHTTPHeader, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-customresponse-syntax.yaml"></a>

```
  [CustomResponseBodyKey](#cfn-wafv2-webacl-customresponse-customresponsebodykey): String
  [ResponseCode](#cfn-wafv2-webacl-customresponse-responsecode): Integer
  [ResponseHeaders](#cfn-wafv2-webacl-customresponse-responseheaders): 
    - CustomHTTPHeader
```

## Properties<a name="aws-properties-wafv2-webacl-customresponse-properties"></a>

`CustomResponseBodyKey`  <a name="cfn-wafv2-webacl-customresponse-customresponsebodykey"></a>
References the response body that you want AWS WAF to return to the web request client\. You can define a custom response for a rule action or a default web ACL action that is set to block\. To do this, you first define the response body key and value in the `CustomResponseBodies` setting for the [AWS::WAFv2::WebACL](aws-resource-wafv2-webacl.md) or [AWS::WAFv2::RuleGroup](aws-resource-wafv2-rulegroup.md) where you want to use it\. Then, in the rule action or web ACL default action `BlockAction` setting, you reference the response body using this key\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseCode`  <a name="cfn-wafv2-webacl-customresponse-responsecode"></a>
The HTTP status code to return to the client\.   
For a list of status codes that you can use in your custom responses, see [Supported status codes for custom response](https://docs.aws.amazon.com/waf/latest/developerguide/customizing-the-response-status-codes.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: Yes  
*Type*: Integer  
*Minimum*: `200`  
*Maximum*: `599`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseHeaders`  <a name="cfn-wafv2-webacl-customresponse-responseheaders"></a>
The HTTP headers to use in the response\. Duplicate header names are not allowed\.   
For information about the limits on count and size for custom request and response settings, see [AWS WAF quotas](https://docs.aws.amazon.com/waf/latest/developerguide/limits.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: List of [CustomHTTPHeader](aws-properties-wafv2-webacl-customhttpheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)