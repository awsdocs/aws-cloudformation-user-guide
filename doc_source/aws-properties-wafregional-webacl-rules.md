# AWS WAF Regional WebACL Rules<a name="aws-properties-wafregional-webacl-rules"></a>

`Rules` is a property of the [AWS::WAFRegional::WebACL](aws-resource-wafregional-webacl.md) resource that specifies the rule to associate with an AWS WAF Regional web access control list \(ACL\) and the rule's settings\.

## Syntax<a name="w3ab2c21c14e2085b5"></a>

### JSON<a name="aws-properties-wafregional-webacl-rules-syntax.json"></a>

```
{
  "[Action](#cfn-wafregional-webacl-rules-action)" : String,
  "[Priority](#cfn-wafregional-webacl-rules-priority)" : Integer,
  "[RuleId](#cfn-wafregional-webacl-rules-ruleid)" : String
}
```

### YAML<a name="aws-properties-wafregional-webacl-rules-syntax.yaml"></a>

```
[Action](#cfn-wafregional-webacl-rules-action): String
[Priority](#cfn-wafregional-webacl-rules-priority): Integer
[RuleId](#cfn-wafregional-webacl-rules-ruleid): String
```

## Properties<a name="w3ab2c21c14e2085b7"></a>

`Action`  <a name="cfn-wafregional-webacl-rules-action"></a>
The action that Amazon CloudFront \(CloudFront\) or AWS WAF takes when a web request matches all conditions in the rule, such as allow, block, or count the request\.  
*Required*: Yes  
*Type*: [AWS WAF Regional WebACL Action](aws-properties-wafregional-webacl-action.md)

`Priority`  <a name="cfn-wafregional-webacl-rules-priority"></a>
The order in which AWS WAF evaluates the rules in a web ACL\. AWS WAF evaluates rules with a lower value before rules with a higher value\. The value must be a unique integer\. If you have multiple rules in a web ACL, the priority numbers do not need to be consecutive\.  
*Required*: Yes  
*Type*: Integer

`RuleId`  <a name="cfn-wafregional-webacl-rules-ruleid"></a>
The ID of an AWS WAF Regional [rule](aws-resource-wafregional-rule.md) to associate with a web ACL\.  
*Required*: Yes  
*Type*: String