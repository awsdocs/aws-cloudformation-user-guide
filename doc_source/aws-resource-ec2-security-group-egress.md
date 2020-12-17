# AWS::EC2::SecurityGroupEgress<a name="aws-resource-ec2-security-group-egress"></a>

\[EC2\-VPC only\] Adds the specified egress rules to a security group for use with a VPC\.

An outbound rule permits instances to send traffic to the specified destination IPv4 or IPv6 CIDR address ranges, or to the specified destination security groups for the same VPC\.

You specify a protocol for each rule \(for example, TCP\)\. For the TCP and UDP protocols, you must also specify the destination port or port range\. For the ICMP protocol, you must also specify the ICMP type and code\. You can use \-1 for the type or code to mean all types or all codes\.

You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\. If you do not specify one of these parameters, the stack will launch successfully but the rule will not be added to the security group\.

Rule changes are propagated to affected instances as quickly as possible\. However, a small delay might occur\.

For more information about VPC security group limits, see [Amazon VPC Limits](https://docs.aws.amazon.com/vpc/latest/userguide/amazon-vpc-limits.html)\.

Use `AWS::EC2::SecurityGroupIngress` and `AWS::EC2::SecurityGroupEgress` only when necessary, typically to allow security groups to reference each other in ingress and egress rules\. Otherwise, use the embedded ingress and egress rules of the security group\. For more information, see [Amazon EC2 Security Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html)\.

## Syntax<a name="aws-resource-ec2-security-group-egress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-security-group-egress-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SecurityGroupEgress",
  "Properties" : {
      "[CidrIp](#cfn-ec2-securitygroupegress-cidrip)" : String,
      "[CidrIpv6](#cfn-ec2-securitygroupegress-cidripv6)" : String,
      "[Description](#cfn-ec2-securitygroupegress-description)" : String,
      "[DestinationPrefixListId](#cfn-ec2-securitygroupegress-destinationprefixlistid)" : String,
      "[DestinationSecurityGroupId](#cfn-ec2-securitygroupegress-destinationsecuritygroupid)" : String,
      "[FromPort](#cfn-ec2-securitygroupegress-fromport)" : Integer,
      "[GroupId](#cfn-ec2-securitygroupegress-groupid)" : String,
      "[IpProtocol](#cfn-ec2-securitygroupegress-ipprotocol)" : String,
      "[ToPort](#cfn-ec2-securitygroupegress-toport)" : Integer
    }
}
```

### YAML<a name="aws-resource-ec2-security-group-egress-syntax.yaml"></a>

```
Type: AWS::EC2::SecurityGroupEgress
Properties: 
  [CidrIp](#cfn-ec2-securitygroupegress-cidrip): String
  [CidrIpv6](#cfn-ec2-securitygroupegress-cidripv6): String
  [Description](#cfn-ec2-securitygroupegress-description): String
  [DestinationPrefixListId](#cfn-ec2-securitygroupegress-destinationprefixlistid): String
  [DestinationSecurityGroupId](#cfn-ec2-securitygroupegress-destinationsecuritygroupid): String
  [FromPort](#cfn-ec2-securitygroupegress-fromport): Integer
  [GroupId](#cfn-ec2-securitygroupegress-groupid): String
  [IpProtocol](#cfn-ec2-securitygroupegress-ipprotocol): String
  [ToPort](#cfn-ec2-securitygroupegress-toport): Integer
```

## Properties<a name="aws-resource-ec2-security-group-egress-properties"></a>

`CidrIp`  <a name="cfn-ec2-securitygroupegress-cidrip"></a>
The IPv4 ranges\.  
You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CidrIpv6`  <a name="cfn-ec2-securitygroupegress-cidripv6"></a>
The IPv6 ranges\.  
You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-securitygroupegress-description"></a>
The description of an egress \(outbound\) security group rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationPrefixListId`  <a name="cfn-ec2-securitygroupegress-destinationprefixlistid"></a>
\[EC2\-VPC only\] The prefix list IDs for an AWS service\. This is the AWS service that you want to access through a VPC endpoint from instances associated with the security group\.  
You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationSecurityGroupId`  <a name="cfn-ec2-securitygroupegress-destinationsecuritygroupid"></a>
The ID of the security group\.  
You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FromPort`  <a name="cfn-ec2-securitygroupegress-fromport"></a>
The start of port range for the TCP and UDP protocols, or an ICMP/ICMPv6 type number\. A value of `-1` indicates all ICMP/ICMPv6 types\. If you specify all ICMP/ICMPv6 types, you must specify all codes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupId`  <a name="cfn-ec2-securitygroupegress-groupid"></a>
The ID of the security group\. You must specify either the security group ID or the security group name in the request\. For security groups in a nondefault VPC, you must specify the security group ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpProtocol`  <a name="cfn-ec2-securitygroupegress-ipprotocol"></a>
The IP protocol name \(`tcp`, `udp`, `icmp`, `icmpv6`\) or number \(see [Protocol Numbers](http://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml)\)\.  
\[VPC only\] Use `-1` to specify all protocols\. When authorizing security group rules, specifying `-1` or a protocol number other than `tcp`, `udp`, `icmp`, or `icmpv6` allows traffic on all ports, regardless of any port range you specify\. For `tcp`, `udp`, and `icmp`, you must specify a port range\. For `icmpv6`, the port range is optional; if you omit the port range, traffic for all types and codes is allowed\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ToPort`  <a name="cfn-ec2-securitygroupegress-toport"></a>
The end of port range for the TCP and UDP protocols, or an ICMP/ICMPv6 code\. A value of `-1` indicates all ICMP/ICMPv6 codes\. If you specify all ICMP/ICMPv6 types, you must specify all codes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-security-group-egress-return-values"></a>

### Ref<a name="aws-resource-ec2-security-group-egress-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the security egress rule\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-security-group-egress--examples"></a>



### VPC Security Groups Example<a name="aws-resource-ec2-security-group-egress--examples--VPC_Security_Groups_Example"></a>

In some cases, you might have an originating \(source\) security group to which you want to add an outbound rule that allows traffic to a destination \(target\) security group\. The target security group also needs an inbound rule that allows traffic from the source security group\. Note that you cannot use the `Ref` function to specify the outbound and inbound rules for each security group\. Doing so creates a circular dependency; you cannot have two resources that depend on each other\. Instead, use the egress and ingress resources to declare these outbound and inbound rules, as shown in the following template example\.

#### JSON<a name="aws-resource-ec2-security-group-egress--examples--VPC_Security_Groups_Example--json"></a>

```
"SourceSG": {
   "Type": "AWS::EC2::SecurityGroup",
   "Properties": {
      "VpcId" : "vpc-1a2b3c4d",
      "GroupDescription": "Sample source security group"
   }
},
"TargetSG": {
   "Type": "AWS::EC2::SecurityGroup",
   "Properties": {
      "VpcId" : "vpc-1a2b3c4d",
      "GroupDescription": "Sample target security group"
   }
},
"OutboundRule": {
   "Type": "AWS::EC2::SecurityGroupEgress",
   "Properties":{
      "IpProtocol": "tcp",
      "FromPort": 0,
      "ToPort": 65535,
      "DestinationSecurityGroupId": {
         "Fn::GetAtt": [
            "TargetSG",
            "GroupId"
         ]
      },
      "GroupId": {
         "Fn::GetAtt": [
            "SourceSG",
            "GroupId"
         ]
      }
   }
},
"InboundRule": {
   "Type": "AWS::EC2::SecurityGroupIngress",
   "Properties":{
      "IpProtocol": "tcp",
      "FromPort": 0,
      "ToPort": 65535,
      "SourceSecurityGroupId": {
         "Fn::GetAtt": [
            "SourceSG",
            "GroupId"
         ]
      },
      "GroupId": {
         "Fn::GetAtt": [
            "TargetSG",
            "GroupId"
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-ec2-security-group-egress--examples--VPC_Security_Groups_Example--yaml"></a>

```
SourceSG:
    Type: AWS::EC2::SecurityGroup
    Properties:
      VpcId: vpc-1a2b3c4d
      GroupDescription: Sample source security group
TargetSG:
    Type: AWS::EC2::SecurityGroup
    Properties:
      VpcId: vpc-1a2b3c4d
      GroupDescription: Sample target security group
OutboundRule:
    Type: AWS::EC2::SecurityGroupEgress
    Properties:
      IpProtocol: tcp
      FromPort: 0
      ToPort: 65535
      DestinationSecurityGroupId:
        Fn::GetAtt:
        - TargetSG
        - GroupId
      GroupId:
        Fn::GetAtt:
        - SourceSG
        - GroupId
InboundRule:
    Type: AWS::EC2::SecurityGroupIngress
    Properties:
      IpProtocol: tcp
      FromPort: 0
      ToPort: 65535
      SourceSecurityGroupId:
        Fn::GetAtt:
        - SourceSG
        - GroupId
      GroupId:
        Fn::GetAtt:
        - TargetSG
        - GroupId
```