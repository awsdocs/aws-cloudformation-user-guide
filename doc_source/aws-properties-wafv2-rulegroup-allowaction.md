# AWS::WAFv2::RuleGroup AllowAction<a name="aws-properties-wafv2-rulegroup-allowaction"></a>

Specifies that AWS WAF should allow the request and optionally defines additional custom handling for the request\.

This is used in the context of other settings, for example to specify values for `RuleAction` and web ACL `DefaultAction`\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-allowaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-allowaction-syntax.json"></a>

```
{
  "[CustomRequestHandling](#cfn-wafv2-rulegroup-allowaction-customrequesthandling)" : CustomRequestHandling
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-allowaction-syntax.yaml"></a>

```
  [CustomRequestHandling](#cfn-wafv2-rulegroup-allowaction-customrequesthandling): 
    CustomRequestHandling
```

## Properties<a name="aws-properties-wafv2-rulegroup-allowaction-properties"></a>

`CustomRequestHandling`  <a name="cfn-wafv2-rulegroup-allowaction-customrequesthandling"></a>
Defines custom handling for the web request\.  
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [CustomRequestHandling](aws-properties-wafv2-rulegroup-customrequesthandling.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)