# AWS::NetworkFirewall::RuleGroup MatchAttributes<a name="aws-properties-networkfirewall-rulegroup-matchattributes"></a>

Criteria for Network Firewall to use to inspect an individual packet in stateless rule inspection\. Each match attributes set can include one or more items such as IP address, CIDR range, port number, protocol, and TCP flags\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-matchattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-matchattributes-syntax.json"></a>

```
{
  "[DestinationPorts](#cfn-networkfirewall-rulegroup-matchattributes-destinationports)" : PortRanges,
  "[Destinations](#cfn-networkfirewall-rulegroup-matchattributes-destinations)" : Addresses,
  "[Protocols](#cfn-networkfirewall-rulegroup-matchattributes-protocols)" : ProtocolNumbers,
  "[SourcePorts](#cfn-networkfirewall-rulegroup-matchattributes-sourceports)" : PortRanges,
  "[Sources](#cfn-networkfirewall-rulegroup-matchattributes-sources)" : Addresses,
  "[TCPFlags](#cfn-networkfirewall-rulegroup-matchattributes-tcpflags)" : TCPFlags
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-matchattributes-syntax.yaml"></a>

```
  [DestinationPorts](#cfn-networkfirewall-rulegroup-matchattributes-destinationports): 
    PortRanges
  [Destinations](#cfn-networkfirewall-rulegroup-matchattributes-destinations): 
    Addresses
  [Protocols](#cfn-networkfirewall-rulegroup-matchattributes-protocols): 
    ProtocolNumbers
  [SourcePorts](#cfn-networkfirewall-rulegroup-matchattributes-sourceports): 
    PortRanges
  [Sources](#cfn-networkfirewall-rulegroup-matchattributes-sources): 
    Addresses
  [TCPFlags](#cfn-networkfirewall-rulegroup-matchattributes-tcpflags): 
    TCPFlags
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-matchattributes-properties"></a>

`DestinationPorts`  <a name="cfn-networkfirewall-rulegroup-matchattributes-destinationports"></a>
The destination ports to inspect for\. If not specified, this matches with any destination port\. This setting is only used for protocols 6 \(TCP\) and 17 \(UDP\)\.   
You can specify individual ports, for example `1994` and you can specify port ranges, for example `1990-1994`\.   
*Required*: No  
*Type*: [PortRanges](aws-properties-networkfirewall-rulegroup-portranges.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destinations`  <a name="cfn-networkfirewall-rulegroup-matchattributes-destinations"></a>
The destination IP addresses and address ranges to inspect for, in CIDR notation\. If not specified, this matches with any destination address\.   
*Required*: No  
*Type*: [Addresses](aws-properties-networkfirewall-rulegroup-addresses.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocols`  <a name="cfn-networkfirewall-rulegroup-matchattributes-protocols"></a>
The protocols to inspect for, specified using each protocol's assigned internet protocol number \(IANA\)\. If not specified, this matches with any protocol\.   
*Required*: No  
*Type*: [ProtocolNumbers](aws-properties-networkfirewall-rulegroup-protocolnumbers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourcePorts`  <a name="cfn-networkfirewall-rulegroup-matchattributes-sourceports"></a>
The source ports to inspect for\. If not specified, this matches with any source port\. This setting is only used for protocols 6 \(TCP\) and 17 \(UDP\)\.   
You can specify individual ports, for example `1994` and you can specify port ranges, for example `1990-1994`\.   
*Required*: No  
*Type*: [PortRanges](aws-properties-networkfirewall-rulegroup-portranges.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sources`  <a name="cfn-networkfirewall-rulegroup-matchattributes-sources"></a>
The source IP addresses and address ranges to inspect for, in CIDR notation\. If not specified, this matches with any source address\.   
*Required*: No  
*Type*: [Addresses](aws-properties-networkfirewall-rulegroup-addresses.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TCPFlags`  <a name="cfn-networkfirewall-rulegroup-matchattributes-tcpflags"></a>
The TCP flags and masks to inspect for\. If not specified, this matches with any settings\. This setting is only used for protocol 6 \(TCP\)\.  
*Required*: No  
*Type*: [TCPFlags](aws-properties-networkfirewall-rulegroup-tcpflags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)