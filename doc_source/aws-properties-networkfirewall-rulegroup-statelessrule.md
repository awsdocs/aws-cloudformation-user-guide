# AWS::NetworkFirewall::RuleGroup StatelessRule<a name="aws-properties-networkfirewall-rulegroup-statelessrule"></a>

A single stateless rule\. This is used in [AWS::NetworkFirewall::RuleGroup StatelessRulesAndCustomActions](aws-properties-networkfirewall-rulegroup-statelessrulesandcustomactions.md)\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-statelessrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-statelessrule-syntax.json"></a>

```
{
  "[Priority](#cfn-networkfirewall-rulegroup-statelessrule-priority)" : Integer,
  "[RuleDefinition](#cfn-networkfirewall-rulegroup-statelessrule-ruledefinition)" : RuleDefinition
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-statelessrule-syntax.yaml"></a>

```
  [Priority](#cfn-networkfirewall-rulegroup-statelessrule-priority): Integer
  [RuleDefinition](#cfn-networkfirewall-rulegroup-statelessrule-ruledefinition): 
    RuleDefinition
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-statelessrule-properties"></a>

`Priority`  <a name="cfn-networkfirewall-rulegroup-statelessrule-priority"></a>
A setting that indicates the order in which to run this rule relative to all of the rules that are defined for a stateless rule group\. Network Firewall evaluates the rules in a rule group starting with the lowest priority setting\. You must ensure that the priority settings are unique for the rule group\.   
Each stateless rule group uses exactly one `StatelessRulesAndCustomActions` object, and each `StatelessRulesAndCustomActions` contains exactly one `StatelessRules` object\. To ensure unique priority settings for your rule groups, set unique priorities for the stateless rules that you define inside any single `StatelessRules` object\.  
You can change the priority settings of your rules at any time\. To make it easier to insert rules later, number them so there's a wide range in between, for example use 100, 200, and so on\.   
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleDefinition`  <a name="cfn-networkfirewall-rulegroup-statelessrule-ruledefinition"></a>
Defines the stateless 5\-tuple packet inspection criteria and the action to take on a packet that matches the criteria\.   
*Required*: Yes  
*Type*: [RuleDefinition](aws-properties-networkfirewall-rulegroup-ruledefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)