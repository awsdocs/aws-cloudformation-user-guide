# AWS::Lightsail::Instance Port<a name="aws-properties-lightsail-instance-port"></a>

`Port` is a property of the [Networking](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-instance-networking.html) property\. It describes information about ports for an instance\.

## Syntax<a name="aws-properties-lightsail-instance-port-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-instance-port-syntax.json"></a>

```
{
  "[AccessDirection](#cfn-lightsail-instance-port-accessdirection)" : String,
  "[AccessFrom](#cfn-lightsail-instance-port-accessfrom)" : String,
  "[AccessType](#cfn-lightsail-instance-port-accesstype)" : String,
  "[CidrListAliases](#cfn-lightsail-instance-port-cidrlistaliases)" : [ String, ... ],
  "[Cidrs](#cfn-lightsail-instance-port-cidrs)" : [ String, ... ],
  "[CommonName](#cfn-lightsail-instance-port-commonname)" : String,
  "[FromPort](#cfn-lightsail-instance-port-fromport)" : Integer,
  "[Ipv6Cidrs](#cfn-lightsail-instance-port-ipv6cidrs)" : [ String, ... ],
  "[Protocol](#cfn-lightsail-instance-port-protocol)" : String,
  "[ToPort](#cfn-lightsail-instance-port-toport)" : Integer
}
```

### YAML<a name="aws-properties-lightsail-instance-port-syntax.yaml"></a>

```
  [AccessDirection](#cfn-lightsail-instance-port-accessdirection): String
  [AccessFrom](#cfn-lightsail-instance-port-accessfrom): String
  [AccessType](#cfn-lightsail-instance-port-accesstype): String
  [CidrListAliases](#cfn-lightsail-instance-port-cidrlistaliases): 
    - String
  [Cidrs](#cfn-lightsail-instance-port-cidrs): 
    - String
  [CommonName](#cfn-lightsail-instance-port-commonname): String
  [FromPort](#cfn-lightsail-instance-port-fromport): Integer
  [Ipv6Cidrs](#cfn-lightsail-instance-port-ipv6cidrs): 
    - String
  [Protocol](#cfn-lightsail-instance-port-protocol): String
  [ToPort](#cfn-lightsail-instance-port-toport): Integer
```

## Properties<a name="aws-properties-lightsail-instance-port-properties"></a>

`AccessDirection`  <a name="cfn-lightsail-instance-port-accessdirection"></a>
The access direction \(`inbound` or `outbound`\)\.  
Lightsail currently supports only `inbound` access direction\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessFrom`  <a name="cfn-lightsail-instance-port-accessfrom"></a>
The location from which access is allowed\. For example, `Anywhere (0.0.0.0/0)`, or `Custom` if a specific IP address or range of IP addresses is allowed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessType`  <a name="cfn-lightsail-instance-port-accesstype"></a>
The type of access \(`Public` or `Private`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CidrListAliases`  <a name="cfn-lightsail-instance-port-cidrlistaliases"></a>
An alias that defines access for a preconfigured range of IP addresses\.  
The only alias currently supported is `lightsail-connect`, which allows IP addresses of the browser\-based RDP/SSH client in the Lightsail console to connect to your instance\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cidrs`  <a name="cfn-lightsail-instance-port-cidrs"></a>
The IPv4 address, or range of IPv4 addresses \(in CIDR notation\) that are allowed to connect to an instance through the ports, and the protocol\.  
The `ipv6Cidrs` parameter lists the IPv6 addresses that are allowed to connect to an instance\.
Examples:  
+ To allow the IP address `192.0.2.44`, specify `192.0.2.44` or `192.0.2.44/32`\. 
+ To allow the IP addresses `192.0.2.0` to `192.0.2.255`, specify `192.0.2.0/24`\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CommonName`  <a name="cfn-lightsail-instance-port-commonname"></a>
The common name of the port information\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FromPort`  <a name="cfn-lightsail-instance-port-fromport"></a>
The first port in a range of open ports on an instance\.  
Allowed ports:  
+ TCP and UDP \- `0` to `65535`
+ ICMP \- The ICMP type for IPv4 addresses\. For example, specify `8` as the `fromPort` \(ICMP type\), and `-1` as the `toPort` \(ICMP code\), to enable ICMP Ping\.
+ ICMPv6 \- The ICMP type for IPv6 addresses\. For example, specify `128` as the `fromPort` \(ICMPv6 type\), and `0` as `toPort` \(ICMPv6 code\)\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ipv6Cidrs`  <a name="cfn-lightsail-instance-port-ipv6cidrs"></a>
The IPv6 address, or range of IPv6 addresses \(in CIDR notation\) that are allowed to connect to an instance through the ports, and the protocol\. Only devices with an IPv6 address can connect to an instance through IPv6; otherwise, IPv4 should be used\.  
The `cidrs` parameter lists the IPv4 addresses that are allowed to connect to an instance\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-lightsail-instance-port-protocol"></a>
The IP protocol name\.  
The name can be one of the following:  
+ `tcp` \- Transmission Control Protocol \(TCP\) provides reliable, ordered, and error\-checked delivery of streamed data between applications running on hosts communicating by an IP network\. If you have an application that doesn't require reliable data stream service, use UDP instead\.
+ `all` \- All transport layer protocol types\.
+ `udp` \- With User Datagram Protocol \(UDP\), computer applications can send messages \(or datagrams\) to other hosts on an Internet Protocol \(IP\) network\. Prior communications are not required to set up transmission channels or data paths\. Applications that don't require reliable data stream service can use UDP, which provides a connectionless datagram service that emphasizes reduced latency over reliability\. If you do require reliable data stream service, use TCP instead\.
+ `icmp` \- Internet Control Message Protocol \(ICMP\) is used to send error messages and operational information indicating success or failure when communicating with an instance\. For example, an error is indicated when an instance could not be reached\. When you specify `icmp` as the `protocol`, you must specify the ICMP type using the `fromPort` parameter, and ICMP code using the `toPort` parameter\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-lightsail-instance-port-toport"></a>
The last port in a range of open ports on an instance\.  
Allowed ports:  
+ TCP and UDP \- `0` to `65535`
+ ICMP \- The ICMP code for IPv4 addresses\. For example, specify `8` as the `fromPort` \(ICMP type\), and `-1` as the `toPort` \(ICMP code\), to enable ICMP Ping\.
+ ICMPv6 \- The ICMP code for IPv6 addresses\. For example, specify `128` as the `fromPort` \(ICMPv6 type\), and `0` as `toPort` \(ICMPv6 code\)\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)