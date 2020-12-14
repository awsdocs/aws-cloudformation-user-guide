# AWS::NetworkFirewall::FirewallPolicy StatefulRuleGroupReference<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference"></a>

Identifier for a single stateful rule group, used in a firewall policy to refer to a rule group\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-syntax.json"></a>

```
{
  "[ResourceArn](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-resourcearn)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-syntax.yaml"></a>

```
  [ResourceArn](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-resourcearn): String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference-properties"></a>

`ResourceArn`  <a name="cfn-networkfirewall-firewallpolicy-statefulrulegroupreference-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the stateful rule group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn:aws.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)