# AWS::WAF::WebACL ActivatedRule<a name="aws-properties-waf-webacl-rules"></a>

The `ActivatedRule` object in an `UpdateWebACL` request specifies a `Rule` that you want to insert or delete, the priority of the `Rule` in the `WebACL`, and the action that you want AWS WAF to take when a web request matches the `Rule` \(`ALLOW`, `BLOCK`, or `COUNT`\)\.

To specify whether to insert or delete a `Rule`, use the `Action` parameter in the `WebACLUpdate` data type\.

## Syntax<a name="aws-properties-waf-webacl-rules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-waf-webacl-rules-syntax.json"></a>

```
{
  "[Action](#cfn-waf-webacl-rules-action)" : WafAction,
  "[Priority](#cfn-waf-webacl-rules-priority)" : Integer,
  "[RuleId](#cfn-waf-webacl-rules-ruleid)" : String
}
```

### YAML<a name="aws-properties-waf-webacl-rules-syntax.yaml"></a>

```
  [Action](#cfn-waf-webacl-rules-action): 
    WafAction
  [Priority](#cfn-waf-webacl-rules-priority): Integer
  [RuleId](#cfn-waf-webacl-rules-ruleid): String
```

## Properties<a name="aws-properties-waf-webacl-rules-properties"></a>

`Action`  <a name="cfn-waf-webacl-rules-action"></a>
Specifies the action that CloudFront or AWS WAF takes when a web request matches the conditions in the `Rule`\. Valid values for `Action` include the following:  
+  `ALLOW`: CloudFront responds with the requested object\.
+  `BLOCK`: CloudFront responds with an HTTP 403 \(Forbidden\) status code\.
+  `COUNT`: AWS WAF increments a counter of requests that match the conditions in the rule and then continues to inspect the web request based on the remaining rules in the web ACL\. 
 `ActivatedRule|OverrideAction` applies only when updating or adding a `RuleGroup` to a `WebACL`\. In this case, you do not use `ActivatedRule|Action`\. For all other update requests, `ActivatedRule|Action` is used instead of `ActivatedRule|OverrideAction`\.  
*Required*: No  
*Type*: [WafAction](aws-properties-waf-webacl-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-waf-webacl-rules-priority"></a>
Specifies the order in which the `Rules` in a `WebACL` are evaluated\. Rules with a lower value for `Priority` are evaluated before `Rules` with a higher value\. The value must be a unique integer\. If you add multiple `Rules` to a `WebACL`, the values don't need to be consecutive\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleId`  <a name="cfn-waf-webacl-rules-ruleid"></a>
The `RuleId` for a `Rule`\. You use `RuleId` to get more information about a `Rule`, update a `Rule`, insert a `Rule` into a `WebACL` or delete a one from a `WebACL`, or delete a `Rule` from AWS WAF\.  
 `RuleId` is returned by `CreateRule` and by `ListRules`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)