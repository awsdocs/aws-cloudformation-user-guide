# AWS::NetworkFirewall::FirewallPolicy StatefulEngineOptions<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions"></a>

Configuration settings for the handling of the stateful rule groups in a firewall policy\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-syntax.json"></a>

```
{
  "[RuleOrder](#cfn-networkfirewall-firewallpolicy-statefulengineoptions-ruleorder)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-syntax.yaml"></a>

```
  [RuleOrder](#cfn-networkfirewall-firewallpolicy-statefulengineoptions-ruleorder): String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-properties"></a>

`RuleOrder`  <a name="cfn-networkfirewall-firewallpolicy-statefulengineoptions-ruleorder"></a>
Indicates how to manage the order of stateful rule evaluation for the policy\. `DEFAULT_ACTION_ORDER` is the default behavior\. Stateful rules are provided to the rule engine as Suricata compatible strings, and Suricata evaluates them based on certain settings\. For more information, see [Evaluation order for stateful rules](https://docs.aws.amazon.com/network-firewall/latest/developerguide/suricata-rule-evaluation-order.html) in the * AWS Network Firewall Developer Guide*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `DEFAULT_ACTION_ORDER | STRICT_ORDER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)