# AWS::NetworkFirewall::FirewallPolicy StatefulEngineOptions<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions"></a>

Configuration settings for the handling of the stateful rule groups in a firewall policy\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-syntax.json"></a>

```
{
  "[RuleOrder](#cfn-networkfirewall-firewallpolicy-statefulengineoptions-ruleorder)" : String,
  "[StreamExceptionPolicy](#cfn-networkfirewall-firewallpolicy-statefulengineoptions-streamexceptionpolicy)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-syntax.yaml"></a>

```
  [RuleOrder](#cfn-networkfirewall-firewallpolicy-statefulengineoptions-ruleorder): String
  [StreamExceptionPolicy](#cfn-networkfirewall-firewallpolicy-statefulengineoptions-streamexceptionpolicy): String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statefulengineoptions-properties"></a>

`RuleOrder`  <a name="cfn-networkfirewall-firewallpolicy-statefulengineoptions-ruleorder"></a>
Indicates how to manage the order of stateful rule evaluation for the policy\. `DEFAULT_ACTION_ORDER` is the default behavior\. Stateful rules are provided to the rule engine as Suricata compatible strings, and Suricata evaluates them based on certain settings\. For more information, see [Evaluation order for stateful rules](https://docs.aws.amazon.com/network-firewall/latest/developerguide/suricata-rule-evaluation-order.html) in the * AWS Network Firewall Developer Guide*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `DEFAULT_ACTION_ORDER | STRICT_ORDER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamExceptionPolicy`  <a name="cfn-networkfirewall-firewallpolicy-statefulengineoptions-streamexceptionpolicy"></a>
Configures how Network Firewall processes traffic when a network connection breaks midstream\. Network connections can break due to disruptions in external networks or within the firewall itself\.  
+ `DROP` \- Network Firewall fails closed and drops all subsequent traffic going to the firewall\. This is the default behavior\.
+ `CONTINUE` \- Network Firewall continues to apply rules to the subsequent traffic without context from traffic before the break\. This impacts the behavior of rules that depend on this context\. For example, if you have a stateful rule to `drop http` traffic, Network Firewall won't match the traffic for this rule because the service won't have the context from session initialization defining the application layer protocol as HTTP\. However, this behavior is rule dependent—a TCP\-layer rule using a `flow:stateless` rule would still match, as would the `aws:drop_strict` default action\.
*Required*: No  
*Type*: String  
*Allowed values*: `CONTINUE | DROP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)