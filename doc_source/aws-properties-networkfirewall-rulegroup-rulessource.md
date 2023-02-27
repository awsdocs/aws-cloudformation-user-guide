# AWS::NetworkFirewall::RuleGroup RulesSource<a name="aws-properties-networkfirewall-rulegroup-rulessource"></a>

The stateless or stateful rules definitions for use in a single rule group\. Each rule group requires a single `RulesSource`\. You can use an instance of this for either stateless rules or stateful rules\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-rulessource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-rulessource-syntax.json"></a>

```
{
  "[RulesSourceList](#cfn-networkfirewall-rulegroup-rulessource-rulessourcelist)" : RulesSourceList,
  "[RulesString](#cfn-networkfirewall-rulegroup-rulessource-rulesstring)" : String,
  "[StatefulRules](#cfn-networkfirewall-rulegroup-rulessource-statefulrules)" : [ StatefulRule, ... ],
  "[StatelessRulesAndCustomActions](#cfn-networkfirewall-rulegroup-rulessource-statelessrulesandcustomactions)" : StatelessRulesAndCustomActions
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-rulessource-syntax.yaml"></a>

```
  [RulesSourceList](#cfn-networkfirewall-rulegroup-rulessource-rulessourcelist): 
    RulesSourceList
  [RulesString](#cfn-networkfirewall-rulegroup-rulessource-rulesstring): 
    String
  [StatefulRules](#cfn-networkfirewall-rulegroup-rulessource-statefulrules): 
    - StatefulRule
  [StatelessRulesAndCustomActions](#cfn-networkfirewall-rulegroup-rulessource-statelessrulesandcustomactions): 
    StatelessRulesAndCustomActions
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-rulessource-properties"></a>

`RulesSourceList`  <a name="cfn-networkfirewall-rulegroup-rulessource-rulessourcelist"></a>
Stateful inspection criteria for a domain list rule group\.   
*Required*: No  
*Type*: [RulesSourceList](aws-properties-networkfirewall-rulegroup-rulessourcelist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RulesString`  <a name="cfn-networkfirewall-rulegroup-rulessource-rulesstring"></a>
Stateful inspection criteria, provided in Suricata compatible intrusion prevention system \(IPS\) rules\. Suricata is an open\-source network IPS that includes a standard rule\-based language for network traffic inspection\.  
These rules contain the inspection criteria and the action to take for traffic that matches the criteria, so this type of rule group doesn't have a separate action setting\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2000000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatefulRules`  <a name="cfn-networkfirewall-rulegroup-rulessource-statefulrules"></a>
An array of individual stateful rules inspection criteria to be used together in a stateful rule group\. Use this option to specify simple Suricata rules with protocol, source and destination, ports, direction, and rule options\. For information about the Suricata `Rules` format, see [Rules Format](https://suricata.readthedocs.io/rules/intro.html#)\.   
*Required*: No  
*Type*: List of [StatefulRule](aws-properties-networkfirewall-rulegroup-statefulrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatelessRulesAndCustomActions`  <a name="cfn-networkfirewall-rulegroup-rulessource-statelessrulesandcustomactions"></a>
Stateless inspection criteria to be used in a stateless rule group\.   
*Required*: No  
*Type*: [StatelessRulesAndCustomActions](aws-properties-networkfirewall-rulegroup-statelessrulesandcustomactions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)