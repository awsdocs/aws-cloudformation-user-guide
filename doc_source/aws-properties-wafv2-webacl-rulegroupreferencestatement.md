# AWS::WAFv2::WebACL RuleGroupReferenceStatement<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement"></a>

A rule statement used to run the rules that are defined in a [AWS::WAFv2::RuleGroup](aws-resource-wafv2-rulegroup.md)\. To use this, create a rule group with your rules, then provide the ARN of the rule group in this statement\.

You cannot nest a `RuleGroupReferenceStatement`, for example for use inside a `NotStatement` or `OrStatement`\. You can only use a rule group reference statement at the top level inside a web ACL\. 

## Syntax<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement-syntax.json"></a>

```
{
  "[Arn](#cfn-wafv2-webacl-rulegroupreferencestatement-arn)" : String,
  "[ExcludedRules](#cfn-wafv2-webacl-rulegroupreferencestatement-excludedrules)" : [ ExcludedRule, ... ],
  "[RuleActionOverrides](#cfn-wafv2-webacl-rulegroupreferencestatement-ruleactionoverrides)" : [ RuleActionOverride, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement-syntax.yaml"></a>

```
  [Arn](#cfn-wafv2-webacl-rulegroupreferencestatement-arn): String
  [ExcludedRules](#cfn-wafv2-webacl-rulegroupreferencestatement-excludedrules): 
    - ExcludedRule
  [RuleActionOverrides](#cfn-wafv2-webacl-rulegroupreferencestatement-ruleactionoverrides): 
    - RuleActionOverride
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
Rules in the referenced rule group whose actions are set to `Count`\.   
Instead of this option, use `RuleActionOverrides`\. It accepts any valid action setting, including `Count`\.
*Required*: No  
*Type*: List of [ExcludedRule](aws-properties-wafv2-webacl-excludedrule.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleActionOverrides`  <a name="cfn-wafv2-webacl-rulegroupreferencestatement-ruleactionoverrides"></a>
Action settings to use in the place of the rule actions that are configured inside the rule group\. You specify one override for each rule whose action you want to change\.   
You can use overrides for testing, for example you can override all of rule actions to `Count` and then monitor the resulting count metrics to understand how the rule group would handle your web traffic\. You can also permanently override some or all actions, to modify how the rule group manages your web traffic\.  
*Required*: No  
*Type*: List of [RuleActionOverride](aws-properties-wafv2-webacl-ruleactionoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)