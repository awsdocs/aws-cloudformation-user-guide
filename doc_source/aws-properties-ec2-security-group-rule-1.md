# AWS::EC2::SecurityGroup Ingress<a name="aws-properties-ec2-security-group-rule-1"></a>

Adds an inbound rule to a security group\.

An inbound rule permits instances to receive traffic from the specified IPv4 or IPv6 CIDR address range, or from the instances associated with the specified security group\.

You must specify only one of the following properties: `CidrIp`, `CidrIpv6`, `SourcePrefixListId`, `SourceSecurityGroupId`, or `SourceSecurityGroupName`\.

You specify a protocol for each rule \(for example, TCP\)\. For TCP and UDP, you must also specify a port or port range\. For ICMP/ICMPv6, you must also specify the ICMP/ICMPv6 type and code\. You can use \-1 to mean all types or all codes\.

You must specify a source security group \(`SourcePrefixListId`, `SourceSecurityGroupId`, or `SourceSecurityGroupName`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\. If you do not specify one of these parameters, the stack will launch successfully but the rule will not be added to the security group\.

Rule changes are propagated to instances within the security group as quickly as possible\. However, a small delay might occur\.

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
You must specify a source security group \(`SourcePrefixListId` or `SourceSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
For examples of rules that you can add to security groups for specific access scenarios, see [Security group rules for different use cases](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/security-group-rules-reference.html) in the *Amazon EC2 User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CidrIpv6`  <a name="cfn-ec2-security-group-rule-cidripv6"></a>
The IPv6 address range, in CIDR format\.  
You must specify a source security group \(`SourcePrefixListId` or `SourceSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
For examples of rules that you can add to security groups for specific access scenarios, see [Security group rules for different use cases](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/security-group-rules-reference.html) in the *Amazon EC2 User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ec2-security-group-rule-description"></a>
Updates the description of an ingress \(inbound\) security group rule\. You can replace an existing description, or add a description to a rule that did not have one previously\.  
Constraints: Up to 255 characters in length\. Allowed characters are a\-z, A\-Z, 0\-9, spaces, and \.\_\-:/\(\)\#,@\[\]\+=;\{\}\!$\*  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FromPort`  <a name="cfn-ec2-security-group-rule-fromport"></a>
If the protocol is TCP or UDP, this is the start of the port range\. If the protocol is ICMP or ICMPv6, this is the type number\. A value of \-1 indicates all ICMP/ICMPv6 types\. If you specify all ICMP/ICMPv6 types, you must specify all ICMP/ICMPv6 codes\.  
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
\[EC2\-VPC only\] The ID of a prefix list\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSecurityGroupId`  <a name="cfn-ec2-security-group-rule-sourcesecuritygroupid"></a>
The ID of the security group\. You must specify either the security group ID or the security group name in the request\. For security groups in a nondefault VPC, you must specify the security group ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSecurityGroupName`  <a name="cfn-ec2-security-group-rule-sourcesecuritygroupname"></a>
\[EC2\-Classic, default VPC\] The name of the source security group\. You can't specify this parameter in combination with an IP address range\. Creates rules that grant full ICMP, UDP, and TCP access\.  
You must specify the `GroupName` property or the `GroupId` property\. For security groups that are in a VPC, you must use the `GroupId` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSecurityGroupOwnerId`  <a name="cfn-ec2-security-group-rule-sourcesecuritygroupownerid"></a>
\[nondefault VPC\] The AWS account ID for the source security group, if the source security group is in a different account\. You can't specify this property with an IP address range\. Creates rules that grant full ICMP, UDP, and TCP access\.  
If you specify `SourceSecurityGroupName` or `SourceSecurityGroupId` and that security group is owned by a different account than the account creating the stack, you must specify the `SourceSecurityGroupOwnerId`; otherwise, this property is optional\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToPort`  <a name="cfn-ec2-security-group-rule-toport"></a>
If the protocol is TCP or UDP, this is the end of the port range\. If the protocol is ICMP or ICMPv6, this is the code\. A value of \-1 indicates all ICMP/ICMPv6 codes\. If you specify all ICMP/ICMPv6 types, you must specify all ICMP/ICMPv6 codes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)