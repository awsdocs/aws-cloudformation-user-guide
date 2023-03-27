# AWS::NetworkFirewall::RuleGroup RuleGroup<a name="aws-properties-networkfirewall-rulegroup-rulegroup"></a>

The object that defines the rules in a rule group\. 

AWS Network Firewall uses a rule group to inspect and control network traffic\. You define stateless rule groups to inspect individual packets and you define stateful rule groups to inspect packets in the context of their traffic flow\. 

To use a rule group, you include it by reference in an Network Firewall firewall policy, then you use the policy in a firewall\. You can reference a rule group from more than one firewall policy, and you can use a firewall policy in more than one firewall\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-rulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-rulegroup-syntax.json"></a>

```
{
  "[ReferenceSets](#cfn-networkfirewall-rulegroup-rulegroup-referencesets)" : ReferenceSets,
  "[RulesSource](#cfn-networkfirewall-rulegroup-rulegroup-rulessource)" : RulesSource,
  "[RuleVariables](#cfn-networkfirewall-rulegroup-rulegroup-rulevariables)" : RuleVariables,
  "[StatefulRuleOptions](#cfn-networkfirewall-rulegroup-rulegroup-statefulruleoptions)" : StatefulRuleOptions
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-rulegroup-syntax.yaml"></a>

```
  [ReferenceSets](#cfn-networkfirewall-rulegroup-rulegroup-referencesets): 
    ReferenceSets
  [RulesSource](#cfn-networkfirewall-rulegroup-rulegroup-rulessource): 
    RulesSource
  [RuleVariables](#cfn-networkfirewall-rulegroup-rulegroup-rulevariables): 
    RuleVariables
  [StatefulRuleOptions](#cfn-networkfirewall-rulegroup-rulegroup-statefulruleoptions): 
    StatefulRuleOptions
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-rulegroup-properties"></a>

`ReferenceSets`  <a name="cfn-networkfirewall-rulegroup-rulegroup-referencesets"></a>
The reference sets for the stateful rule group\.  
*Required*: No  
*Type*: [ReferenceSets](aws-properties-networkfirewall-rulegroup-referencesets.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RulesSource`  <a name="cfn-networkfirewall-rulegroup-rulegroup-rulessource"></a>
The stateful rules or stateless rules for the rule group\.   
*Required*: Yes  
*Type*: [RulesSource](aws-properties-networkfirewall-rulegroup-rulessource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleVariables`  <a name="cfn-networkfirewall-rulegroup-rulegroup-rulevariables"></a>
Settings that are available for use in the rules in the rule group\. You can only use these for stateful rule groups\.   
*Required*: No  
*Type*: [RuleVariables](aws-properties-networkfirewall-rulegroup-rulevariables.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatefulRuleOptions`  <a name="cfn-networkfirewall-rulegroup-rulegroup-statefulruleoptions"></a>
Additional options governing how Network Firewall handles stateful rules\. The policies where you use your stateful rule group must have stateful rule options settings that are compatible with these settings\.  
*Required*: No  
*Type*: [StatefulRuleOptions](aws-properties-networkfirewall-rulegroup-statefulruleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)