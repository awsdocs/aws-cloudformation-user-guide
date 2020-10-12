# AWS::WAFv2::WebACL RuleGroupReferenceStatement<a name="aws-properties-wafv2-webacl-rulegroupreferencestatement"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A rule statement used to run the rules that are defined in a RuleGroup\. To use this, create a rule group with your rules, then provide the ARN of the rule group in this statement\.

You cannot nest a `RuleGroupReferenceStatement`, for example for use inside a `NotStatement` or `OrStatement`\. It can only be referenced as a top\-level statement within a rule\.

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
The names of rules that are in the referenced rule group, but that you want AWS WAF to exclude from processing for this rule statement\.   
*Required*: No  
*Type*: List of [ExcludedRule](aws-properties-wafv2-webacl-excludedrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)