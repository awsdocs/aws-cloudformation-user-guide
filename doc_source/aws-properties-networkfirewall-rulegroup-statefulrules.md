# AWS::NetworkFirewall::RuleGroup StatefulRules<a name="aws-properties-networkfirewall-rulegroup-statefulrules"></a>

5\-tuple stateful rules, for use in a stateful rule group\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-statefulrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-statefulrules-syntax.json"></a>

```
{
  "[StatefulRules](#cfn-networkfirewall-rulegroup-statefulrules-statefulrules)" : [ StatefulRule, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-statefulrules-syntax.yaml"></a>

```
  [StatefulRules](#cfn-networkfirewall-rulegroup-statefulrules-statefulrules): 
    - StatefulRule
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-statefulrules-properties"></a>

`StatefulRules`  <a name="cfn-networkfirewall-rulegroup-statefulrules-statefulrules"></a>
5\-tuple stateful rules\.  
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-statefulrules) of [StatefulRule](aws-properties-networkfirewall-rulegroup-statefulrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)