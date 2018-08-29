# AWS WAF WebACL Action<a name="aws-properties-waf-webacl-action"></a>

`Action` is a property of the [AWS::WAF::WebACL](aws-resource-waf-webacl.md) resource and the [AWS WAF WebACL Rules](aws-properties-waf-webacl-rules.md) property that specifies the action AWS WAF takes when a web request matches or doesn't match all rule conditions\.

## Syntax<a name="w3ab2c21c14e2032b5"></a>

### JSON<a name="aws-properties-waf-webacl-action-syntax.json"></a>

```
{
  "[Type](#cfn-waf-webacl-action-type)" : String
}
```

### YAML<a name="aws-properties-waf-webacl-action-syntax.yaml"></a>

```
[Type](#cfn-waf-webacl-action-type): String
```

## Properties<a name="w3ab2c21c14e2032b7"></a>

`Type`  <a name="cfn-waf-webacl-action-type"></a>
For actions that are associated with a rule, the action that AWS WAF takes when a web request matches all conditions in a rule\.  
For the default action of a web access control list \(ACL\), the action that AWS WAF takes when a web request doesn't match all conditions in any rule\.  
For valid value, see the `Type` contents of the [WafAction](http://docs.aws.amazon.com/waf/latest/APIReference/API_WafAction.html) data type in the *AWS WAF API Reference*\.  
*Required*: Yes  
*Type*: String