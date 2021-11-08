# AWS::NetworkFirewall::RuleGroup StatefulRuleOptions<a name="aws-properties-networkfirewall-rulegroup-statefulruleoptions"></a>

Additional options governing how Network Firewall handles the rule group\. You can only use these for stateful rule groups\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-statefulruleoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-statefulruleoptions-syntax.json"></a>

```
{
  "[RuleOrder](#cfn-networkfirewall-rulegroup-statefulruleoptions-ruleorder)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-statefulruleoptions-syntax.yaml"></a>

```
  [RuleOrder](#cfn-networkfirewall-rulegroup-statefulruleoptions-ruleorder): String
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-statefulruleoptions-properties"></a>

`RuleOrder`  <a name="cfn-networkfirewall-rulegroup-statefulruleoptions-ruleorder"></a>
Indicates how to manage the order of the rule evaluation for the rule group\. `DEFAULT_ACTION_ORDER` is the default behavior\. Stateful rules are provided to the rule engine as Suricata compatible strings, and Suricata evaluates them based on certain settings\. For more information, see [Evaluation order for stateful rules](https://docs.aws.amazon.com/network-firewall/latest/developerguide/suricata-rule-evaluation-order.html) in the *AWS Network Firewall Developer Guide*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `DEFAULT_ACTION_ORDER | STRICT_ORDER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)