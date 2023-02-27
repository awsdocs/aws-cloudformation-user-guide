# AWS::NetworkFirewall::FirewallPolicy StatefulRuleGroupReference<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference"></a>

Identifier for a single stateful rule group, used in a firewall policy to refer to a rule group\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-syntax.json"></a>

```
{
  "[Override](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-override)" : StatefulRuleGroupOverride,
  "[Priority](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-priority)" : Integer,
  "[ResourceArn](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-resourcearn)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-syntax.yaml"></a>

```
  [Override](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-override): 
    StatefulRuleGroupOverride
  [Priority](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-priority): Integer
  [ResourceArn](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-resourcearn): String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-properties"></a>

`Override`  <a name="cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-override"></a>
The action that allows the policy owner to override the behavior of the rule group within a policy\.  
*Required*: No  
*Type*: [StatefulRuleGroupOverride](aws-properties-networkfirewall-firewallpolicy-statefulrulegroupoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-priority"></a>
An integer setting that indicates the order in which to run the stateful rule groups in a single [AWS::NetworkFirewall::FirewallPolicy](aws-resource-networkfirewall-firewallpolicy.md)\. This setting only applies to firewall policies that specify the `STRICT_ORDER` rule order in the stateful engine options settings\.  
Network Firewall evalutes each stateful rule group against a packet starting with the group that has the lowest priority setting\. You must ensure that the priority settings are unique within each policy\.  
You can change the priority settings of your rule groups at any time\. To make it easier to insert rule groups later, number them so there's a wide range in between, for example use 100, 200, and so on\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceArn`  <a name="cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the stateful rule group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn:aws.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)