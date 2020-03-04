# AWS::EC2::SecurityGroup Egress<a name="aws-properties-ec2-security-group-rule"></a>

Specifies an outbound rule for a security group\. An outbound rule permits instances to send traffic to the specified IPv4 or IPv6 CIDR address ranges, or to the instances associated with the specified destination security groups\.

You must specify only one of the following properties: `CidrIp`, `CidrIpv6`, `DestinationPrefixListId`, or `DestinationSecurityGroupId`\.

The EC2 Security Group Rule is an embedded property of the `AWS::EC2::SecurityGroup` type\.

## Syntax<a name="aws-properties-ec2-security-group-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-security-group-rule-syntax.json"></a>

```
{
  "[CidrIp](#cfn-ec2-security-group-rule-cidrip)" : String,
  "[CidrIpv6](#cfn-ec2-security-group-rule-cidripv6)" : String,
  "[Description](#cfn-ec2-security-group-rule-description)" : String,
  "[DestinationPrefixListId](#cfn-ec2-security-group-rule-destinationprefixlistid)" : String,
  "[DestinationSecurityGroupId](#cfn-ec2-security-group-rule-destsecgroupid)" : String,
  "[FromPort](#cfn-ec2-security-group-rule-fromport)" : Integer,
  "[IpProtocol](#cfn-ec2-security-group-rule-ipprotocol)" : String,
  "[ToPort](#cfn-ec2-security-group-rule-toport)" : Integer
}
```

### YAML<a name="aws-properties-ec2-security-group-rule-syntax.yaml"></a>

```
  [CidrIp](#cfn-ec2-security-group-rule-cidrip): String
  [CidrIpv6](#cfn-ec2-security-group-rule-cidripv6): String
  [Description](#cfn-ec2-security-group-rule-description): String
  [DestinationPrefixListId](#cfn-ec2-security-group-rule-destinationprefixlistid): String
  [DestinationSecurityGroupId](#cfn-ec2-security-group-rule-destsecgroupid): String
  [FromPort](#cfn-ec2-security-group-rule-fromport): Integer
  [IpProtocol](#cfn-ec2-security-group-rule-ipprotocol): String
  [ToPort](#cfn-ec2-security-group-rule-toport): Integer
```

## Properties<a name="aws-properties-ec2-security-group-rule-properties"></a>

`CidrIp`  <a name="cfn-ec2-security-group-rule-cidrip"></a>
The destination IPv4 address range, in CIDR format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CidrIpv6`  <a name="cfn-ec2-security-group-rule-cidripv6"></a>
\[EC2\-VPC only\] The IPv6 ranges\.  
The destination IPv6 address range, in CIDR format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ec2-security-group-rule-description"></a>
A description for the security group rule\.  
Constraints: Up to 255 characters in length\. Allowed characters are a\-z, A\-Z, 0\-9, spaces, and \.\_\-:/\(\)\#,@\[\]\+=;\{\}\!$\*  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationPrefixListId`  <a name="cfn-ec2-security-group-rule-destinationprefixlistid"></a>
\[EC2\-VPC only\] The prefix list IDs for the destination AWS service\. This is the AWS service that you want to access through a VPC endpoint from instances associated with the security group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationSecurityGroupId`  <a name="cfn-ec2-security-group-rule-destsecgroupid"></a>
The ID of the destination VPC security group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FromPort`  <a name="cfn-ec2-security-group-rule-fromport"></a>
The start of port range for the TCP and UDP protocols, or an ICMP/ICMPv6 type number\. A value of `-1` indicates all ICMP/ICMPv6 types\. If you specify all ICMP/ICMPv6 types, you must specify all codes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpProtocol`  <a name="cfn-ec2-security-group-rule-ipprotocol"></a>
The IP protocol name \(`tcp`, `udp`, `icmp`, `icmpv6`\) or number \(see [Protocol Numbers](http://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml)\)\.  
\[VPC only\] Use `-1` to specify all protocols\. When authorizing security group rules, specifying `-1` or a protocol number other than `tcp`, `udp`, `icmp`, or `icmpv6` allows traffic on all ports, regardless of any port range you specify\. For `tcp`, `udp`, and `icmp`, you must specify a port range\. For `icmpv6`, the port range is optional; if you omit the port range, traffic for all types and codes is allowed\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-ec2-security-group-rule-toport"></a>
The end of port range for the TCP and UDP protocols, or an ICMP/ICMPv6 code\. A value of `-1` indicates all ICMP/ICMPv6 codes\. If you specify all ICMP/ICMPv6 types, you must specify all codes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)