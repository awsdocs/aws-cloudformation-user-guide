# AWS::NetworkFirewall::FirewallPolicy StatelessRuleGroupReference<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreference"></a>

Identifier for a single stateless rule group, used in a firewall policy to refer to the rule group\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreference-syntax.json"></a>

```
{
  "[Priority](#cfn-networkfirewall-firewallpolicy-statelessrulegroupreference-priority)" : Integer,
  "[ResourceArn](#cfn-networkfirewall-firewallpolicy-statelessrulegroupreference-resourcearn)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreference-syntax.yaml"></a>

```
  [Priority](#cfn-networkfirewall-firewallpolicy-statelessrulegroupreference-priority): Integer
  [ResourceArn](#cfn-networkfirewall-firewallpolicy-statelessrulegroupreference-resourcearn): String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreference-properties"></a>

`Priority`  <a name="cfn-networkfirewall-firewallpolicy-statelessrulegroupreference-priority"></a>
An integer setting that indicates the order in which to run the stateless rule groups in a single [AWS::NetworkFirewall::FirewallPolicy](aws-resource-networkfirewall-firewallpolicy.md)\. Network Firewall applies each stateless rule group to a packet starting with the group that has the lowest priority setting\. You must ensure that the priority settings are unique within each policy\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceArn`  <a name="cfn-networkfirewall-firewallpolicy-statelessrulegroupreference-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the stateless rule group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn:aws.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)