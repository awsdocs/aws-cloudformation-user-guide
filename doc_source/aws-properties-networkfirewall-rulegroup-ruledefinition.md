# AWS::NetworkFirewall::RuleGroup RuleDefinition<a name="aws-properties-networkfirewall-rulegroup-ruledefinition"></a>

The inspection criteria and action for a single stateless rule\. AWS Network Firewall inspects each packet for the specified matching criteria\. When a packet matches the criteria, Network Firewall performs the rule's actions on the packet\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-ruledefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-ruledefinition-syntax.json"></a>

```
{
  "[Actions](#cfn-networkfirewall-rulegroup-ruledefinition-actions)" : [ String, ... ],
  "[MatchAttributes](#cfn-networkfirewall-rulegroup-ruledefinition-matchattributes)" : MatchAttributes
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-ruledefinition-syntax.yaml"></a>

```
  [Actions](#cfn-networkfirewall-rulegroup-ruledefinition-actions): 
    - String
  [MatchAttributes](#cfn-networkfirewall-rulegroup-ruledefinition-matchattributes): 
    MatchAttributes
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-ruledefinition-properties"></a>

`Actions`  <a name="cfn-networkfirewall-rulegroup-ruledefinition-actions"></a>
The actions to take on a packet that matches one of the stateless rule definition's match attributes\. You must specify a standard action and you can add custom actions\.   
Network Firewall only forwards a packet for stateful rule inspection if you specify `aws:forward_to_sfe` for a rule that the packet matches, or if the packet doesn't match any stateless rule and you specify `aws:forward_to_sfe` for the `StatelessDefaultActions` setting for the [AWS::NetworkFirewall::FirewallPolicy](aws-resource-networkfirewall-firewallpolicy.md)\.
For every rule, you must specify exactly one of the following standard actions\.   
+  **aws:pass** \- Discontinues all inspection of the packet and permits it to go to its intended destination\.
+  **aws:drop** \- Discontinues all inspection of the packet and blocks it from going to its intended destination\.
+  **aws:forward\_to\_sfe** \- Discontinues stateless inspection of the packet and forwards it to the stateful rule engine for inspection\. 
Additionally, you can specify a custom action\. To do this, you define a custom action by name and type, then provide the name you've assigned to the action in this `Actions` setting\.   
To provide more than one action in this setting, separate the settings with a comma\. For example, if you have a publish metrics custom action that you've named `MyMetricsAction`, then you could specify the standard action `aws:pass` combined with the custom action using `[“aws:pass”, “MyMetricsAction”]`\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchAttributes`  <a name="cfn-networkfirewall-rulegroup-ruledefinition-matchattributes"></a>
Criteria for Network Firewall to use to inspect an individual packet in stateless rule inspection\. Each match attributes set can include one or more items such as IP address, CIDR range, port number, protocol, and TCP flags\.   
*Required*: Yes  
*Type*: [MatchAttributes](aws-properties-networkfirewall-rulegroup-matchattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)