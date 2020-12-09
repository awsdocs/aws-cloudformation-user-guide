# AWS::NetworkFirewall::RuleGroup Header<a name="aws-properties-networkfirewall-rulegroup-header"></a>

The 5\-tuple criteria for AWS Network Firewall to use to inspect packet headers in stateful traffic flow inspection\. Traffic flows that match the criteria are a match for the corresponding stateful rule\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-header-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-header-syntax.json"></a>

```
{
  "[Destination](#cfn-networkfirewall-rulegroup-header-destination)" : String,
  "[DestinationPort](#cfn-networkfirewall-rulegroup-header-destinationport)" : String,
  "[Direction](#cfn-networkfirewall-rulegroup-header-direction)" : String,
  "[Protocol](#cfn-networkfirewall-rulegroup-header-protocol)" : String,
  "[Source](#cfn-networkfirewall-rulegroup-header-source)" : String,
  "[SourcePort](#cfn-networkfirewall-rulegroup-header-sourceport)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-header-syntax.yaml"></a>

```
  [Destination](#cfn-networkfirewall-rulegroup-header-destination): String
  [DestinationPort](#cfn-networkfirewall-rulegroup-header-destinationport): String
  [Direction](#cfn-networkfirewall-rulegroup-header-direction): String
  [Protocol](#cfn-networkfirewall-rulegroup-header-protocol): String
  [Source](#cfn-networkfirewall-rulegroup-header-source): String
  [SourcePort](#cfn-networkfirewall-rulegroup-header-sourceport): String
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-header-properties"></a>

`Destination`  <a name="cfn-networkfirewall-rulegroup-header-destination"></a>
The destination IP address or address range to inspect for, in CIDR notation\. To match with any address, specify `ANY`\.   
Specify an IP address or a block of IP addresses in Classless Inter\-Domain Routing \(CIDR\) notation\. Network Firewall supports all address ranges for IPv4\.   
Examples:   
+ To configure Network Firewall to inspect for the IP address 192\.0\.2\.44, specify `192.0.2.44/32`\.
+ To configure Network Firewall to inspect for IP addresses from 192\.0\.2\.0 to 192\.0\.2\.255, specify `192.0.2.0/24`\.
For more information about CIDR notation, see the Wikipedia entry [Classless Inter\-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationPort`  <a name="cfn-networkfirewall-rulegroup-header-destinationport"></a>
The destination port to inspect for\. You can specify an individual port, for example `1994` and you can specify a port range, for example `1990-1994`\. To match with any port, specify `ANY`\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Direction`  <a name="cfn-networkfirewall-rulegroup-header-direction"></a>
The direction of traffic flow to inspect\. If set to `ANY`, the inspection matches bidirectional traffic, both from the source to the destination and from the destination to the source\. If set to `FORWARD`, the inspection only matches traffic going from the source to the destination\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ANY | FORWARD`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-networkfirewall-rulegroup-header-protocol"></a>
The protocol to inspect for\. To match with any protocol, specify `ANY`\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `DCERPC | DHCP | DNS | FTP | HTTP | ICMP | IKEV2 | IMAP | IP | KRB5 | MSN | NTP | SMB | SMTP | SSH | TCP | TFTP | TLS | UDP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-networkfirewall-rulegroup-header-source"></a>
The source IP address or address range to inspect for, in CIDR notation\. To match with any address, specify `ANY`\.   
Specify an IP address or a block of IP addresses in Classless Inter\-Domain Routing \(CIDR\) notation\. Network Firewall supports all address ranges for IPv4\.   
Examples:   
+ To configure Network Firewall to inspect for the IP address 192\.0\.2\.44, specify `192.0.2.44/32`\.
+ To configure Network Firewall to inspect for IP addresses from 192\.0\.2\.0 to 192\.0\.2\.255, specify `192.0.2.0/24`\.
For more information about CIDR notation, see the Wikipedia entry [Classless Inter\-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourcePort`  <a name="cfn-networkfirewall-rulegroup-header-sourceport"></a>
The source port to inspect for\. You can specify an individual port, for example `1994` and you can specify a port range, for example `1990-1994`\. To match with any port, specify `ANY`\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)