# AWS::WAF::WebACL WafAction<a name="aws-properties-waf-webacl-action"></a>

**Note**  
This is **AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF**, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

For the action that is associated with a rule in a `WebACL`, specifies the action that you want AWS WAF to perform when a web request matches all of the conditions in a rule\. For the default action in a `WebACL`, specifies the action that you want AWS WAF to take when a web request doesn't match all of the conditions in any of the rules in a `WebACL`\. 

## Syntax<a name="aws-properties-waf-webacl-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-waf-webacl-action-properties"></a>

`Type`  <a name="cfn-waf-webacl-action-type"></a>
Specifies how you want AWS WAF to respond to requests that match the settings in a `Rule`\. Valid settings include the following:  
+  `ALLOW`: AWS WAF allows requests
+  `BLOCK`: AWS WAF blocks requests
+  `COUNT`: AWS WAF increments a counter of the requests that match all of the conditions in the rule\. AWS WAF then continues to inspect the web request based on the remaining rules in the web ACL\. You can't specify `COUNT` for the default action for a `WebACL`\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALLOW | BLOCK | COUNT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)