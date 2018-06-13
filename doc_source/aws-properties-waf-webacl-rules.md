# AWS WAF WebACL Rules<a name="aws-properties-waf-webacl-rules"></a>

`Rules` is a property of the [AWS::WAF::WebACL](aws-resource-waf-webacl.md) resource that specifies the rule to associate with an AWS WAF web access control list \(ACL\) and the rule's settings\.

## Syntax<a name="w3ab2c21c14e2036b5"></a>

### JSON<a name="aws-properties-waf-webacl-rules-syntax.json"></a>

```
{
  "[Action](#cfn-waf-webacl-rules-action)" : AWS WAF WebACL Action
  "[Priority](#cfn-waf-webacl-rules-priority)" : Integer,
  "[RuleId](#cfn-waf-webacl-rules-ruleid)" : String
}
```

### YAML<a name="aws-properties-waf-webacl-rules-syntax.yaml"></a>

```
[Action](#cfn-waf-webacl-rules-action): AWS WAF WebACL Action
[Priority](#cfn-waf-webacl-rules-priority): Integer
[RuleId](#cfn-waf-webacl-rules-ruleid): String
```

## Properties<a name="w3ab2c21c14e2036b7"></a>

`Action`  <a name="cfn-waf-webacl-rules-action"></a>
The action that Amazon CloudFront \(CloudFront\) or AWS WAF takes when a web request matches all conditions in the rule, such as allow, block, or count the request\.  
*Required*: Yes  
*Type*: [AWS WAF WebACL Action](aws-properties-waf-webacl-action.md)

`Priority`  <a name="cfn-waf-webacl-rules-priority"></a>
The order in which AWS WAF evaluates the rules in a web ACL\. AWS WAF evaluates rules with a lower value before rules with a higher value\. The value must be a unique integer\. If you have multiple rules in a web ACL, the priority numbers do not need to be consecutive\.  
*Required*: Yes  
*Type*: Integer

`RuleId`  <a name="cfn-waf-webacl-rules-ruleid"></a>
The ID of an AWS WAF [rule](aws-resource-waf-rule.md) to associate with a web ACL\.  
*Required*: Yes  
*Type*: String