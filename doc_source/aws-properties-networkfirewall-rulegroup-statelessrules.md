# AWS::NetworkFirewall::RuleGroup StatelessRules<a name="aws-properties-networkfirewall-rulegroup-statelessrules"></a>

The stateless rules in a rule group\. This is used in [AWS::NetworkFirewall::RuleGroup StatelessRulesAndCustomActions](aws-properties-networkfirewall-rulegroup-statelessrulesandcustomactions.md)\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-statelessrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-statelessrules-syntax.json"></a>

```
{
  "[StatelessRules](#cfn-networkfirewall-rulegroup-statelessrules-statelessrules)" : [ StatelessRule, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-statelessrules-syntax.yaml"></a>

```
  [StatelessRules](#cfn-networkfirewall-rulegroup-statelessrules-statelessrules): 
    - StatelessRule
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-statelessrules-properties"></a>

`StatelessRules`  <a name="cfn-networkfirewall-rulegroup-statelessrules-statelessrules"></a>
The stateless rules\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-statelessrules) of [StatelessRule](aws-properties-networkfirewall-rulegroup-statelessrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)