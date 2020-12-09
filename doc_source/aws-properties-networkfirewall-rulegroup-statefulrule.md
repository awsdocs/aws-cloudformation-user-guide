# AWS::NetworkFirewall::RuleGroup StatefulRule<a name="aws-properties-networkfirewall-rulegroup-statefulrule"></a>

A single 5\-tuple stateful rule, for use in a stateful rule group\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-statefulrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-statefulrule-syntax.json"></a>

```
{
  "[Action](#cfn-networkfirewall-rulegroup-statefulrule-action)" : String,
  "[Header](#cfn-networkfirewall-rulegroup-statefulrule-header)" : Header,
  "[RuleOptions](#cfn-networkfirewall-rulegroup-statefulrule-ruleoptions)" : RuleOptions
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-statefulrule-syntax.yaml"></a>

```
  [Action](#cfn-networkfirewall-rulegroup-statefulrule-action): String
  [Header](#cfn-networkfirewall-rulegroup-statefulrule-header): 
    Header
  [RuleOptions](#cfn-networkfirewall-rulegroup-statefulrule-ruleoptions): 
    RuleOptions
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-statefulrule-properties"></a>

`Action`  <a name="cfn-networkfirewall-rulegroup-statefulrule-action"></a>
Defines what Network Firewall should do with the packets in a traffic flow when the flow matches the stateful rule criteria\. For all actions, Network Firewall performs the specified action and discontinues stateful inspection of the traffic flow\.   
The actions for a stateful rule are defined as follows:   
+  **PASS** \- Permits the packets to go to the intended destination\.
+  **DROP** \- Blocks the packets from going to the intended destination and sends an alert log message, if alert logging is configured in the firewall's [AWS::NetworkFirewall::LoggingConfiguration](aws-resource-networkfirewall-loggingconfiguration.md)\. 
+  **ALERT** \- Permits the packets to go to the intended destination and sends an alert log message, if alert logging is configured in the firewall's [AWS::NetworkFirewall::LoggingConfiguration](aws-resource-networkfirewall-loggingconfiguration.md)\. 

  You can use this action to test a rule that you intend to use to drop traffic\. You can enable the rule with `ALERT` action, verify in the logs that the rule is filtering as you want, then change the action to `DROP`\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALERT | DROP | PASS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Header`  <a name="cfn-networkfirewall-rulegroup-statefulrule-header"></a>
The stateful 5\-tuple inspection criteria for this rule, used to inspect traffic flows\.   
*Required*: Yes  
*Type*: [Header](aws-properties-networkfirewall-rulegroup-header.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleOptions`  <a name="cfn-networkfirewall-rulegroup-statefulrule-ruleoptions"></a>
Additional settings for a stateful rule, provided as keywords and settings\.   
*Required*: Yes  
*Type*: [RuleOptions](aws-properties-networkfirewall-rulegroup-ruleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)