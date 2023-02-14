# AWS::WAFRegional::WebACL Rule<a name="aws-properties-wafregional-webacl-rule"></a>

A combination of `ByteMatchSet`, `IPSet`, and/or `SqlInjectionMatchSet` objects that identify the web requests that you want to allow, block, or count\. For example, you might create a `Rule` that includes the following predicates:
+ An `IPSet` that causes AWS WAF to search for web requests that originate from the IP address `192.0.2.44` 
+ A `ByteMatchSet` that causes AWS WAF to search for web requests for which the value of the `User-Agent` header is `BadBot`\.

To match the settings in this `Rule`, a request must originate from `192.0.2.44` AND include a `User-Agent` header for which the value is `BadBot`\.

## Syntax<a name="aws-properties-wafregional-webacl-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafregional-webacl-rule-syntax.json"></a>

```
{
  "[Action](#cfn-wafregional-webacl-rule-action)" : Action,
  "[Priority](#cfn-wafregional-webacl-rule-priority)" : Integer,
  "[RuleId](#cfn-wafregional-webacl-rule-ruleid)" : String
}
```

### YAML<a name="aws-properties-wafregional-webacl-rule-syntax.yaml"></a>

```
  [Action](#cfn-wafregional-webacl-rule-action): 
    Action
  [Priority](#cfn-wafregional-webacl-rule-priority): Integer
  [RuleId](#cfn-wafregional-webacl-rule-ruleid): String
```

## Properties<a name="aws-properties-wafregional-webacl-rule-properties"></a>

`Action`  <a name="cfn-wafregional-webacl-rule-action"></a>
The action that AWS WAF takes when a web request matches all conditions in the rule, such as allow, block, or count the request\.  
*Required*: Yes  
*Type*: [Action](aws-properties-wafregional-webacl-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-wafregional-webacl-rule-priority"></a>
The order in which AWS WAF evaluates the rules in a web ACL\. AWS WAF evaluates rules with a lower value before rules with a higher value\. The value must be a unique integer\. If you have multiple rules in a web ACL, the priority numbers do not need to be consecutive\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleId`  <a name="cfn-wafregional-webacl-rule-ruleid"></a>
The ID of an AWS WAF Regional rule to associate with a web ACL\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)