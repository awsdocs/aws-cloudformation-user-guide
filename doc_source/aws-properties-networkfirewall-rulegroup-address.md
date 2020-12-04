# AWS::NetworkFirewall::RuleGroup Address<a name="aws-properties-networkfirewall-rulegroup-address"></a>

A single IP address specification\. This is used in the [AWS::NetworkFirewall::RuleGroup MatchAttributes](aws-properties-networkfirewall-rulegroup-matchattributes.md) source and destination specifications\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-address-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-address-syntax.json"></a>

```
{
  "[AddressDefinition](#cfn-networkfirewall-rulegroup-address-addressdefinition)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-address-syntax.yaml"></a>

```
  [AddressDefinition](#cfn-networkfirewall-rulegroup-address-addressdefinition): String
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-address-properties"></a>

`AddressDefinition`  <a name="cfn-networkfirewall-rulegroup-address-addressdefinition"></a>
Specify an IP address or a block of IP addresses in Classless Inter\-Domain Routing \(CIDR\) notation\. Network Firewall supports all address ranges for IPv4\.   
Examples:   
+ To configure Network Firewall to inspect for the IP address 192\.0\.2\.44, specify `192.0.2.44/32`\.
+ To configure Network Firewall to inspect for IP addresses from 192\.0\.2\.0 to 192\.0\.2\.255, specify `192.0.2.0/24`\.
For more information about CIDR notation, see the Wikipedia entry [Classless Inter\-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^([a-fA-F\d:\.]+/\d{1,3})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)