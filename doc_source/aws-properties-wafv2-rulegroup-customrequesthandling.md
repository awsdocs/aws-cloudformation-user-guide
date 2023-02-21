# AWS::WAFv2::RuleGroup CustomRequestHandling<a name="aws-properties-wafv2-rulegroup-customrequesthandling"></a>

Custom request handling behavior that inserts custom headers into a web request\. You can add custom request handling for AWS WAF to use when the rule action doesn't block the request\. For example, `CaptchaAction` for requests with valid t okens, and `AllowAction`\. 

For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-customrequesthandling-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-customrequesthandling-syntax.json"></a>

```
{
  "[InsertHeaders](#cfn-wafv2-rulegroup-customrequesthandling-insertheaders)" : [ CustomHTTPHeader, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-customrequesthandling-syntax.yaml"></a>

```
  [InsertHeaders](#cfn-wafv2-rulegroup-customrequesthandling-insertheaders): 
    - CustomHTTPHeader
```

## Properties<a name="aws-properties-wafv2-rulegroup-customrequesthandling-properties"></a>

`InsertHeaders`  <a name="cfn-wafv2-rulegroup-customrequesthandling-insertheaders"></a>
The HTTP headers to insert into the request\. Duplicate header names are not allowed\.   
For information about the limits on count and size for custom request and response settings, see [AWS WAF quotas](https://docs.aws.amazon.com/waf/latest/developerguide/limits.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: Yes  
*Type*: List of [CustomHTTPHeader](aws-properties-wafv2-rulegroup-customhttpheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)