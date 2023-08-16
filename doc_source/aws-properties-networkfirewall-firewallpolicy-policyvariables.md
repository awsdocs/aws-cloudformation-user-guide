# AWS::NetworkFirewall::FirewallPolicy PolicyVariables<a name="aws-properties-networkfirewall-firewallpolicy-policyvariables"></a>

Contains variables that you can use to override default Suricata settings in your firewall policy\.

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-policyvariables-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-policyvariables-syntax.json"></a>

```
{
  "[RuleVariables](#cfn-networkfirewall-firewallpolicy-policyvariables-rulevariables)" : {Key: Value, ...}
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-policyvariables-syntax.yaml"></a>

```
  [RuleVariables](#cfn-networkfirewall-firewallpolicy-policyvariables-rulevariables): 
    Key: Value
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-policyvariables-properties"></a>

`RuleVariables`  <a name="cfn-networkfirewall-firewallpolicy-policyvariables-rulevariables"></a>
The IPv4 or IPv6 addresses in CIDR notation to use for the Suricata `HOME_NET` variable\. If your firewall uses an inspection VPC, you might want to override the `HOME_NET` variable with the CIDRs of your home networks\. If you don't override `HOME_NET` with your own CIDRs, Network Firewall by default uses the CIDR of your inspection VPC\.  
*Required*: No  
*Type*: Map of [IPSet](aws-properties-networkfirewall-firewallpolicy-ipset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)