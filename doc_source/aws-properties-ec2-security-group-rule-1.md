# AWS::EC2::SecurityGroup Ingress<a name="aws-properties-ec2-security-group-rule-1"></a>

Specifies an inbound rule for a security group\. An inbound rule permits instances to receive traffic from the specified IPv4 or IPv6 CIDR address ranges, or from the instances associated with the specified source security groups\.

You must specify only one of the following properties: `CidrIp`, `CidrIpv6`, `SourcePrefixListId`, `SourceSecurityGroupId`, or `SourceSecurityGroupName`\.

The EC2 Security Group Rule is an embedded property of the `AWS::EC2::SecurityGroup` type\.

## Syntax<a name="aws-properties-ec2-security-group-rule-1-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-security-group-rule-1-syntax.json"></a>

```
{
  "[CidrIp](#cfn-ec2-security-group-rule-cidrip)" : String,
  "[CidrIpv6](#cfn-ec2-security-group-rule-cidripv6)" : String,
  "[Description](#cfn-ec2-security-group-rule-description)" : String,
  "[FromPort](#cfn-ec2-security-group-rule-fromport)" : Integer,
  "[IpProtocol](#cfn-ec2-security-group-rule-ipprotocol)" : String,
  "[SourcePrefixListId](#cfn-ec2-securitygroup-ingress-sourceprefixlistid)" : String,
  "[SourceSecurityGroupId](#cfn-ec2-security-group-rule-sourcesecuritygroupid)" : String,
  "[SourceSecurityGroupName](#cfn-ec2-security-group-rule-sourcesecuritygroupname)" : String,
  "[SourceSecurityGroupOwnerId](#cfn-ec2-security-group-rule-sourcesecuritygroupownerid)" : String,
  "[ToPort](#cfn-ec2-security-group-rule-toport)" : Integer
}
```

### YAML<a name="aws-properties-ec2-security-group-rule-1-syntax.yaml"></a>

```
  [CidrIp](#cfn-ec2-security-group-rule-cidrip): String
  [CidrIpv6](#cfn-ec2-security-group-rule-cidripv6): String
  [Description](#cfn-ec2-security-group-rule-description): String
  [FromPort](#cfn-ec2-security-group-rule-fromport): Integer
  [IpProtocol](#cfn-ec2-security-group-rule-ipprotocol): String
  [SourcePrefixListId](#cfn-ec2-securitygroup-ingress-sourceprefixlistid): String
  [SourceSecurityGroupId](#cfn-ec2-security-group-rule-sourcesecuritygroupid): String
  [SourceSecurityGroupName](#cfn-ec2-security-group-rule-sourcesecuritygroupname): String
  [SourceSecurityGroupOwnerId](#cfn-ec2-security-group-rule-sourcesecuritygroupownerid): String
  [ToPort](#cfn-ec2-security-group-rule-toport): Integer
```

## Properties<a name="aws-properties-ec2-security-group-rule-1-properties"></a>

`CidrIp`  <a name="cfn-ec2-security-group-rule-cidrip"></a>
The IPv4 address range, in CIDR format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CidrIpv6`  <a name="cfn-ec2-security-group-rule-cidripv6"></a>
The IPv6 address range, in CIDR format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ec2-security-group-rule-description"></a>
A description for the security group rule\.  
Constraints: Up to 255 characters in length\. Allowed characters are a\-z, A\-Z, 0\-9, spaces, and \.\_\-:/\(\)\#,@\[\]\+=;\{\}\!$\*  
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

`SourcePrefixListId`  <a name="cfn-ec2-securitygroup-ingress-sourceprefixlistid"></a>
\[EC2\-VPC only\] The prefix list IDs for an AWS service\. This is the AWS service that you want to access through a VPC endpoint from instances associated with the security group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSecurityGroupId`  <a name="cfn-ec2-security-group-rule-sourcesecuritygroupid"></a>
 *For VPC security groups only*\. The ID of the security group to allow access\. You can use the `Ref` intrinsic function to refer to the logical ID of a security group defined in the same template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSecurityGroupName`  <a name="cfn-ec2-security-group-rule-sourcesecuritygroupname"></a>
\[EC2\-Classic, default VPC\] The name of the source security group\. You can't specify this parameter in combination with the following parameters: the CIDR IP address range, the start of the port range, the IP protocol, and the end of the port range\. Creates rules that grant full ICMP, UDP, and TCP access\. To create a rule with a specific IP protocol and port range, use a set of IP permissions instead\. For EC2\-VPC, the source security group must be in the same VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSecurityGroupOwnerId`  <a name="cfn-ec2-security-group-rule-sourcesecuritygroupownerid"></a>
The AWS account ID of the owner of the security group that is specified in the `SourceSecurityGroupName` property\.  
If you specify `SourceSecurityGroupName` and that security group is owned by a different account than the account creating the stack, you must specify the `SourceSecurityGroupOwnerId`; otherwise, this property is optional\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-ec2-security-group-rule-toport"></a>
The end of port range for the TCP and UDP protocols, or an ICMP/ICMPv6 code\. A value of `-1` indicates all ICMP/ICMPv6 codes\. If you specify all ICMP/ICMPv6 types, you must specify all codes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)