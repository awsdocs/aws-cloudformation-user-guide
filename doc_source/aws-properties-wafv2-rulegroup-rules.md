# AWS::WAFv2::RuleGroup Rules<a name="aws-properties-wafv2-rulegroup-rules"></a>

Array of rules\.

## Syntax<a name="aws-properties-wafv2-rulegroup-rules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-rules-syntax.json"></a>

```
{
  "[Rules](#cfn-wafv2-rulegroup-rules-rules)" : [ [Rule](aws-properties-wafv2-rulegroup-rule.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-rules-syntax.yaml"></a>

```
  [Rules](#cfn-wafv2-rulegroup-rules-rules): 
    - [Rule](aws-properties-wafv2-rulegroup-rule.md)
```

## Properties<a name="aws-properties-wafv2-rulegroup-rules-properties"></a>

`Rules`  <a name="cfn-wafv2-rulegroup-rules-rules"></a>
Array of rules\.   
*Required*: No  
*Type*: [List](#aws-properties-wafv2-rulegroup-rules) of [Rule](aws-properties-wafv2-rulegroup-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)