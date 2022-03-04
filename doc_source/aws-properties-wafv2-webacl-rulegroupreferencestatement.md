# AWS::WAFv2::WebACL RuleGroupReferenceStatement<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement"></a>

A rule statement used to run the rules that are defined in a [AWS::WAFv2::RuleGroup](aws-resource-wafv2-rulegroup.md)\. To use this, create a rule group with your rules, then provide the ARN of the rule group in this statement\.

You cannot nest a `RuleGroupReferenceStatement`, for example for use inside a `NotStatement` or `OrStatement`\. You can only use a rule group reference statement at the top level inside a web ACL\. 

## Syntax<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement-syntax.json"></a>

```
{
  "[Arn](#cfn-wafv2-webacl-rulegroupreferencestatement-arn)" : String,
  "[ExcludedRules](#cfn-wafv2-webacl-rulegroupreferencestatement-excludedrules)" : [ ExcludedRule, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement-syntax.yaml"></a>

```
  [Arn](#cfn-wafv2-webacl-rulegroupreferencestatement-arn): String
  [ExcludedRules](#cfn-wafv2-webacl-rulegroupreferencestatement-excludedrules): 
    - ExcludedRule
```

## Properties<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement-properties"></a>

`Arn`  <a name="cfn-wafv2-webacl-rulegroupreferencestatement-arn"></a>
The Amazon Resource Name \(ARN\) of the entity\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludedRules`  <a name="cfn-wafv2-webacl-rulegroupreferencestatement-excludedrules"></a>
The rules in the referenced rule group whose actions are set to `Count`\. When you exclude a rule, AWS WAF evaluates it exactly as it would if the rule action setting were `Count`\. This is a useful option for testing the rules in a rule group without modifying how they handle your web traffic\.  
*Required*: No  
*Type*: List of [ExcludedRule](aws-properties-wafv2-webacl-excludedrule.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)