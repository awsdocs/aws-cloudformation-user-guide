# AWS::EC2::SecurityGroupEgress<a name="aws-resource-ec2-security-group-egress"></a>

The `AWS::EC2::SecurityGroupEgress` resource adds an egress rule to an Amazon VPC security group\.

**Important**  
Use `AWS::EC2::SecurityGroupIngress` and `AWS::EC2::SecurityGroupEgress` only when necessary, typically to allow security groups to reference each other in ingress and egress rules\. Otherwise, use the embedded ingress and egress rules of [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md)\. For more information, see [Amazon EC2 Security Groups](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html)\.

**Topics**
+ [Syntax](#aws-resource-ec2-securitygroupegress-syntax)
+ [Properties](#w3ab2c21c10d470c11)
+ [Return Values](#w3ab2c21c10d470c13)
+ [VPC Security Groups Example](#w3ab2c21c10d470c15)

## Syntax<a name="aws-resource-ec2-securitygroupegress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-securitygroupegress-syntax.json"></a>

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

### YAML<a name="aws-resource-ec2-securitygroupegress-syntax.yaml"></a>

```
Type: "AWS::EC2::SecurityGroupEgress"
Properties:
  [CidrIp](#cfn-ec2-securitygroupegress-cidrip): String
  [CidrIpv6](#cfn-ec2-securitygroupegress-cidripv6): String
  [Description](#cfn-ec2-securitygroupegress-description): String
  [DestinationPrefixListId](#cfn-ec2-securitygroupegress-destinationprefixlistid): String
  [DestinationSecurityGroupId](#cfn-ec2-securitygroupegress-destinationsecuritygroupid):  String
  [FromPort](#cfn-ec2-securitygroupegress-fromport): Integer
  [GroupId](#cfn-ec2-securitygroupegress-groupid): String
  [IpProtocol](#cfn-ec2-securitygroupegress-ipprotocol): String
  [ToPort](#cfn-ec2-securitygroupegress-toport): Integer
```

## Properties<a name="w3ab2c21c10d470c11"></a>

For more information about adding egress rules to VPC security groups, go to [AuthorizeSecurityGroupEgress](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AuthorizeSecurityGroupEgress.html) in the *Amazon EC2 API Reference*\.

**Note**  
If you change this resource's logical ID, you must also update a property value in order to trigger an update for this resource\.

`CidrIp`  <a name="cfn-ec2-securitygroupegress-cidrip"></a>
An IPv4 CIDR range\.  
*Required*: Conditional\. You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CidrIpv6`  <a name="cfn-ec2-securitygroupegress-cidripv6"></a>
An IPv6 CIDR range\.  
*Type*: String  
*Required*: Conditional\. You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-ec2-securitygroupegress-description"></a>
Description of the egress rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DestinationPrefixListId`  <a name="cfn-ec2-securitygroupegress-destinationprefixlistid"></a>
The AWS service prefix of an Amazon VPC endpoint\. For more information, see [VPC Endpoints](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-endpoints.html) in the *Amazon VPC User Guide*\.  
*Required*: Conditional\. You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DestinationSecurityGroupId`  <a name="cfn-ec2-securitygroupegress-destinationsecuritygroupid"></a>
Specifies the group ID of the destination Amazon VPC security group\.  
*Required*: Conditional\. You must specify a destination security group \(`DestinationPrefixListId` or `DestinationSecurityGroupId`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`FromPort`  <a name="cfn-ec2-securitygroupegress-fromport"></a>
Start of port range for the TCP and UDP protocols, or an ICMP type number\. If you specify `icmp` for the `IpProtocol` property, you can specify \-1 as a wildcard \(i\.e\., any ICMP type number\)\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`GroupId`  <a name="cfn-ec2-securitygroupegress-groupid"></a>
ID of the Amazon VPC security group to modify\. This value can be a reference to an [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md) resource that has a valid `VpcId` property or the ID of an existing Amazon VPC security group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`IpProtocol`  <a name="cfn-ec2-securitygroupegress-ipprotocol"></a>
IP protocol name or number\. For valid values, see the IpProtocol parameter in [AuthorizeSecurityGroupIngress](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AuthorizeSecurityGroupIngress.html)  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ToPort`  <a name="cfn-ec2-securitygroupegress-toport"></a>
End of port range for the TCP and UDP protocols, or an ICMP code\. If you specify `icmp` for the `IpProtocol` property, you can specify \-1 as a wildcard \(i\.e\., any ICMP code\)\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d470c13"></a>

### Ref<a name="w3ab2c21c10d470c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## VPC Security Groups Example<a name="w3ab2c21c10d470c15"></a>

In some cases, you might have an originating \(source\) security group to which you want to add an outbound rule that allows traffic to a destination \(target\) security group\. The target security group also needs an inbound rule that allows traffic from the source security group\. Note that you cannot use the `Ref` function to specify the outbound and inbound rules for each security group\. Doing so creates a circular dependency; you cannot have two resources that depend on each other\. Instead, use the egress and ingress resources to declare these outbound and inbound rules, as shown in the following template snippet\.

### JSON<a name="aws-resource-ec2-securitygroupegress-example-1.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "SourceSG": {
      "Type": "AWS::EC2::SecurityGroup",
      "Properties": {
        "VpcId" : "vpc-e063f789",
        "GroupDescription": "Sample source security group"
      }
    },
    "TargetSG": {
      "Type": "AWS::EC2::SecurityGroup",
      "Properties": {
        "VpcId" : "vpc-e063f789",
        "GroupDescription": "Sample target security group"
      }
    },
    "OutboundRule": {
      "Type": "AWS::EC2::SecurityGroupEgress",
      "Properties":{
        "IpProtocol": "tcp",
        "FromPort": "0",
        "ToPort": "65535",
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
        "FromPort": "0",
        "ToPort": "65535",
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
  }
}
```

### YAML<a name="aws-resource-ec2-securitygroupegress-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  SourceSG:
    Type: AWS::EC2::SecurityGroup
    Properties:
      VpcId: vpc-e063f789
      GroupDescription: Sample source security group
  TargetSG:
    Type: AWS::EC2::SecurityGroup
    Properties:
      VpcId: vpc-e063f789
      GroupDescription: Sample target security group
  OutboundRule:
    Type: AWS::EC2::SecurityGroupEgress
    Properties:
      IpProtocol: tcp
      FromPort: '0'
      ToPort: '65535'
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
      FromPort: '0'
      ToPort: '65535'
      SourceSecurityGroupId:
        Fn::GetAtt:
        - SourceSG
        - GroupId
      GroupId:
        Fn::GetAtt:
        - TargetSG
        - GroupId
```