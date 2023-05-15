# AWS::NetworkFirewall::FirewallPolicy IPSet<a name="aws-properties-networkfirewall-firewallpolicy-ipset"></a>

A list of IP addresses and address ranges, in CIDR notation\. This is part of a [RuleVariables](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-networkfirewall-rulegroup-rulegroup.html#cfn-networkfirewall-rulegroup-rulegroup-rulevariables)\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-ipset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-ipset-syntax.json"></a>

```
{
  "[Definition](#cfn-networkfirewall-firewallpolicy-ipset-definition)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-ipset-syntax.yaml"></a>

```
  [Definition](#cfn-networkfirewall-firewallpolicy-ipset-definition): 
    - String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-ipset-properties"></a>

`Definition`  <a name="cfn-networkfirewall-firewallpolicy-ipset-definition"></a>
The list of IP addresses and address ranges, in CIDR notation\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)