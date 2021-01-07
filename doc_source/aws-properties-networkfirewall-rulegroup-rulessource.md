# AWS::NetworkFirewall::RuleGroup RulesSource<a name="aws-properties-networkfirewall-rulegroup-rulessource"></a>

The stateless or stateful rules definitions for use in a single rule group\. Each rule group requires a single `RulesSource`\. You can use an instance of this for either stateless rules or stateful rules\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-rulessource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-rulessource-syntax.json"></a>

```
{
  "[RulesSourceList](#cfn-networkfirewall-rulegroup-rulessource-rulessourcelist)" : RulesSourceList,
  "[RulesString](#cfn-networkfirewall-rulegroup-rulessource-rulesstring)" : String,
  "[StatefulRules](#cfn-networkfirewall-rulegroup-rulessource-statefulrules)" : StatefulRules,
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
    StatefulRules
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
You can provide the rules from a file that you've stored in an Amazon S3 bucket, or by providing the rules in a Suricata rules string\. To import from Amazon S3, provide the fully qualified name of the file that contains the rules definitions\. To provide a Suricata rule string, provide the complete, Suricata compatible rule\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatefulRules`  <a name="cfn-networkfirewall-rulegroup-rulessource-statefulrules"></a>
The 5\-tuple stateful inspection criteria\. This contains an array of individual 5\-tuple stateful rules to be used together in a stateful rule group\.   
*Required*: No  
*Type*: [StatefulRules](aws-properties-networkfirewall-rulegroup-statefulrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatelessRulesAndCustomActions`  <a name="cfn-networkfirewall-rulegroup-rulessource-statelessrulesandcustomactions"></a>
Stateless inspection criteria to be used in a stateless rule group\.   
*Required*: No  
*Type*: [StatelessRulesAndCustomActions](aws-properties-networkfirewall-rulegroup-statelessrulesandcustomactions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)