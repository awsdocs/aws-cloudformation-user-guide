# AWS::WAFRegional::WebACL Action<a name="aws-properties-wafregional-webacl-action"></a>

Specifies the action AWS WAF takes when a web request matches or doesn't match all rule conditions\. 

## Syntax<a name="aws-properties-wafregional-webacl-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafregional-webacl-action-syntax.json"></a>

```
{
  "[Type](#cfn-wafregional-webacl-action-type)" : String
}
```

### YAML<a name="aws-properties-wafregional-webacl-action-syntax.yaml"></a>

```
  [Type](#cfn-wafregional-webacl-action-type): String
```

## Properties<a name="aws-properties-wafregional-webacl-action-properties"></a>

`Type`  <a name="cfn-wafregional-webacl-action-type"></a>
For actions that are associated with a rule, the action that AWS WAF takes when a web request matches all conditions in a rule\.  
For the default action of a web access control list \(ACL\), the action that AWS WAF takes when a web request doesn't match all conditions in any rule\.   
Valid settings include the following:  
+  `ALLOW`: AWS WAF allows requests
+  `BLOCK`: AWS WAF blocks requests
+  `COUNT`: AWS WAF increments a counter of the requests that match all of the conditions in the rule\. AWS WAF then continues to inspect the web request based on the remaining rules in the web ACL\. You can't specify `COUNT` for the default action for a WebACL\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)