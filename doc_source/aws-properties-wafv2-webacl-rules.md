# AWS::WAFv2::WebACL Rules<a name="aws-properties-wafv2-webacl-rules"></a>

You use a rule in a WebACL or RuleGroup to identify web requests that you want to allow, block, or count\. Each rule includes one top\-level statement that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles the matches\.

## Syntax<a name="aws-properties-wafv2-webacl-rules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-rules-syntax.json"></a>

```
{
  "[Rules](#cfn-wafv2-webacl-rules-rules)" : [ [Rule](aws-properties-wafv2-webacl-rule.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-rules-syntax.yaml"></a>

```
  [Rules](#cfn-wafv2-webacl-rules-rules): 
    - [Rule](aws-properties-wafv2-webacl-rule.md)
```

## Properties<a name="aws-properties-wafv2-webacl-rules-properties"></a>

`Rules`  <a name="cfn-wafv2-webacl-rules-rules"></a>
You use a rule in a WebACL or RuleGroup to identify web requests that you want to allow, block, or count\. Each rule includes one top\-level statement that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles the matches  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-webacl-rules) of [Rule](aws-properties-wafv2-webacl-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)