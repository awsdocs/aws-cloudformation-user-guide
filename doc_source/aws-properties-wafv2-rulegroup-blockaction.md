# AWS::WAFv2::RuleGroup BlockAction<a name="aws-properties-wafv2-rulegroup-blockaction"></a>

Specifies that AWS WAF should block the request and optionally defines additional custom handling for the response to the web request\.

This is used in the context of other settings, for example to specify values for `RuleAction` and web ACL `DefaultAction`\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-blockaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-blockaction-syntax.json"></a>

```
{
  "[CustomResponse](#cfn-wafv2-rulegroup-blockaction-customresponse)" : CustomResponse
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-blockaction-syntax.yaml"></a>

```
  [CustomResponse](#cfn-wafv2-rulegroup-blockaction-customresponse): 
    CustomResponse
```

## Properties<a name="aws-properties-wafv2-rulegroup-blockaction-properties"></a>

`CustomResponse`  <a name="cfn-wafv2-rulegroup-blockaction-customresponse"></a>
Defines a custom response for the web request\.  
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [CustomResponse](aws-properties-wafv2-rulegroup-customresponse.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)