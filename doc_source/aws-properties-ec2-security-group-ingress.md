# AWS::EC2::SecurityGroupIngress<a name="aws-properties-ec2-security-group-ingress"></a>

Adds an inbound rule to a security group\.

An inbound rule permits instances to receive traffic from the specified IPv4 or IPv6 CIDR address range, or from the instances associated with the specified security group\.

You specify a protocol for each rule \(for example, TCP\)\. For TCP and UDP, you must also specify a port or port range\. For ICMP/ICMPv6, you must also specify the ICMP/ICMPv6 type and code\. You can use \-1 to mean all types or all codes\.

You must specify a source security group \(`SourcePrefixListId`, `SourceSecurityGroupId`, or `SourceSecurityGroupName`\) or a CIDR range \(`CidrIp` or `CidrIpv6`\)\. If you do not specify one of these parameters, the stack will launch successfully but the rule will not be added to the security group\.

Rule changes are propagated to instances within the security group as quickly as possible\. However, a small delay might occur\.

## Syntax<a name="aws-properties-ec2-security-group-ingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-security-group-ingress-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SecurityGroupIngress",
  "Properties" : {
      "[CidrIp](#cfn-ec2-security-group-ingress-cidrip)" : String,
      "[CidrIpv6](#cfn-ec2-security-group-ingress-cidripv6)" : String,
      "[Description](#cfn-ec2-security-group-ingress-description)" : String,
      "[FromPort](#cfn-ec2-security-group-ingress-fromport)" : Integer,
      "[GroupId](#cfn-ec2-security-group-ingress-groupid)" : String,
      "[GroupName](#cfn-ec2-security-group-ingress-groupname)" : String,
      "[IpProtocol](#cfn-ec2-security-group-ingress-ipprotocol)" : String,
      "[SourcePrefixListId](#cfn-ec2-securitygroupingress-sourceprefixlistid)" : String,
      "[SourceSecurityGroupId](#cfn-ec2-security-group-ingress-sourcesecuritygroupid)" : String,
      "[SourceSecurityGroupName](#cfn-ec2-security-group-ingress-sourcesecuritygroupname)" : String,
      "[SourceSecurityGroupOwnerId](#cfn-ec2-security-group-ingress-sourcesecuritygroupownerid)" : String,
      "[ToPort](#cfn-ec2-security-group-ingress-toport)" : Integer
    }
}
```

### YAML<a name="aws-properties-ec2-security-group-ingress-syntax.yaml"></a>

```
Type: AWS::EC2::SecurityGroupIngress
Properties: 
  [CidrIp](#cfn-ec2-security-group-ingress-cidrip): String
  [CidrIpv6](#cfn-ec2-security-group-ingress-cidripv6): String
  [Description](#cfn-ec2-security-group-ingress-description): String
  [FromPort](#cfn-ec2-security-group-ingress-fromport): Integer
  [GroupId](#cfn-ec2-security-group-ingress-groupid): String
  [GroupName](#cfn-ec2-security-group-ingress-groupname): String
  [IpProtocol](#cfn-ec2-security-group-ingress-ipprotocol): String
  [SourcePrefixListId](#cfn-ec2-securitygroupingress-sourceprefixlistid): String
  [SourceSecurityGroupId](#cfn-ec2-security-group-ingress-sourcesecuritygroupid): String
  [SourceSecurityGroupName](#cfn-ec2-security-group-ingress-sourcesecuritygroupname): String
  [SourceSecurityGroupOwnerId](#cfn-ec2-security-group-ingress-sourcesecuritygroupownerid): String
  [ToPort](#cfn-ec2-security-group-ingress-toport): Integer
```

## Properties<a name="aws-properties-ec2-security-group-ingress-properties"></a>

`CidrIp`  <a name="cfn-ec2-security-group-ingress-cidrip"></a>
The IPv4 ranges\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CidrIpv6`  <a name="cfn-ec2-security-group-ingress-cidripv6"></a>
\[VPC only\] The IPv6 ranges\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-security-group-ingress-description"></a>
Updates the description of an ingress \(inbound\) security group rule\. You can replace an existing description, or add a description to a rule that did not have one previously\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FromPort`  <a name="cfn-ec2-security-group-ingress-fromport"></a>
The start of port range for the TCP and UDP protocols, or an ICMP/ICMPv6 type number\. A value of `-1` indicates all ICMP/ICMPv6 types\. If you specify all ICMP/ICMPv6 types, you must specify all codes\.  
Use this for ICMP and any protocol that uses ports\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupId`  <a name="cfn-ec2-security-group-ingress-groupid"></a>
The ID of the security group\. You must specify either the security group ID or the security group name in the request\. For security groups in a nondefault VPC, you must specify the security group ID\.  
You must specify the `GroupName` property or the `GroupId` property\. For security groups that are in a VPC, you must use the `GroupId` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupName`  <a name="cfn-ec2-security-group-ingress-groupname"></a>
The name of the security group\.  
Constraints: Up to 255 characters in length\. Cannot start with `sg-`\.  
Constraints for EC2\-Classic: ASCII characters  
Constraints for EC2\-VPC: a\-z, A\-Z, 0\-9, spaces, and \.\_\-:/\(\)\#,@\[\]\+=&;\{\}\!$\*  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpProtocol`  <a name="cfn-ec2-security-group-ingress-ipprotocol"></a>
The IP protocol name \(`tcp`, `udp`, `icmp`, `icmpv6`\) or number \(see [Protocol Numbers](http://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml)\)\.  
\[VPC only\] Use `-1` to specify all protocols\. When authorizing security group rules, specifying `-1` or a protocol number other than `tcp`, `udp`, `icmp`, or `icmpv6` allows traffic on all ports, regardless of any port range you specify\. For `tcp`, `udp`, and `icmp`, you must specify a port range\. For `icmpv6`, the port range is optional; if you omit the port range, traffic for all types and codes is allowed\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourcePrefixListId`  <a name="cfn-ec2-securitygroupingress-sourceprefixlistid"></a>
\[EC2\-VPC only\] The ID of a prefix list\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceSecurityGroupId`  <a name="cfn-ec2-security-group-ingress-sourcesecuritygroupid"></a>
The ID of the security group\. You must specify either the security group ID or the security group name\. For security groups in a nondefault VPC, you must specify the security group ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceSecurityGroupName`  <a name="cfn-ec2-security-group-ingress-sourcesecuritygroupname"></a>
\[EC2\-Classic, default VPC\] The name of the source security group\.  
You must specify the `GroupName` property or the `GroupId` property\. For security groups that are in a VPC, you must use the `GroupId` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceSecurityGroupOwnerId`  <a name="cfn-ec2-security-group-ingress-sourcesecuritygroupownerid"></a>
\[nondefault VPC\] The AWS account ID that owns the source security group\. You can't specify this property with an IP address range\.  
If you specify `SourceSecurityGroupName` or `SourceSecurityGroupId` and that security group is owned by a different account than the account creating the stack, you must specify the `SourceSecurityGroupOwnerId`; otherwise, this property is optional\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ToPort`  <a name="cfn-ec2-security-group-ingress-toport"></a>
The end of port range for the TCP and UDP protocols, or an ICMP/ICMPv6 code\. A value of `-1` indicates all ICMP/ICMPv6 codes for the specified ICMP type\. If you specify all ICMP/ICMPv6 types, you must specify all codes\.  
Use this for ICMP and any protocol that uses ports\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-properties-ec2-security-group-ingress--examples"></a>



### EC2 Security Group and Ingress Rule<a name="aws-properties-ec2-security-group-ingress--examples--EC2_Security_Group_and_Ingress_Rule"></a>

To declare an Amazon EC2 \(non\-VPC\) security group and an ingress rule, use the `SourceSecurityGroupName ` property in the ingress rule\.

The following template example defines an EC2 security group with an ingress rule that allows incoming traffic on port 80 from any other host in the security group\. 

#### JSON<a name="aws-properties-ec2-security-group-ingress--examples--EC2_Security_Group_and_Ingress_Rule--json"></a>

```
"SGBase": {
   "Type": "AWS::EC2::SecurityGroup",
   "Properties": {
      "GroupDescription": "Base Security Group",
      "SecurityGroupIngress": [
         {
            "IpProtocol": "tcp",
            "CidrIp": "0.0.0.0/0",
            "FromPort": 22,
            "ToPort": 22
         }
      ]
   }
},
"SGBaseIngress": {
   "Type": "AWS::EC2::SecurityGroupIngress",
   "Properties": {
      "GroupId": {
         "Ref": "SGBase"
      },
      "IpProtocol": "tcp",
      "FromPort": 80,
      "ToPort": 80,
      "SourceSecurityGroupId": {
         "Fn::GetAtt": [
            "SGBase",
            "GroupId"
         ]
      }
   } 
}
```

#### YAML<a name="aws-properties-ec2-security-group-ingress--examples--EC2_Security_Group_and_Ingress_Rule--yaml"></a>

```
SGBase:
   Type: 'AWS::EC2::SecurityGroup'
   Properties:
      GroupDescription: Base Security Group
      SecurityGroupIngress:
         - IpProtocol: tcp
           CidrIp: 0.0.0.0/0
           FromPort: 22
           ToPort: 22
SGBaseIngress:
   Type: 'AWS::EC2::SecurityGroupIngress'
   Properties:
      GroupId: !Ref SGBase
      IpProtocol: tcp
      FromPort: 80
      ToPort: 80
      SourceSecurityGroupId: !GetAtt SGBase.GroupId
```

### Allow Traffic from a Security Group in a Peered VPC<a name="aws-properties-ec2-security-group-ingress--examples--Allow_Traffic_from_a_Security_Group_in_a_Peered_VPC"></a>

Like the previous example, the following example allows one\-way traffic from an originating \(source\) security group to a destination \(target\) security group\. However, in this example the security groups are in peered VPCs across AWS accounts\. You might want to allow cross\-account traffic if, for example, you create a security scanning resource in one AWS account that you'll use to run diagnostics in another account\. This example adds an ingress rule to a target VPC security group that allows incoming traffic from a source security group in a different AWS account\. Note that the source security group also needs an egress rule that allows outgoing traffic to the target security group\. Because the source security group is in a different account, the following example doesn't use the Ref function to reference the source security group ID but instead directly specifies the security group ID `sg-12345678`\. 

#### JSON<a name="aws-properties-ec2-security-group-ingress--examples--Allow_Traffic_from_a_Security_Group_in_a_Peered_VPC--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "TargetSG": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "VpcId": "vpc-1a2b3c4d",
                "GroupDescription": "Security group allowing ingress for security scanners"
            }
        },
        "InboundRule": {
            "Type": "AWS::EC2::SecurityGroupIngress",
            "Properties": {
                "GroupId": {
                    "Fn::GetAtt": [
                        "TargetSG",
                        "GroupId"
                    ]
                },
                "IpProtocol": "tcp",
                "FromPort": "80",
                "ToPort": "80",
                "SourceSecurityGroupId": "sg-12345678",
                "SourceSecurityGroupOwnerId": "123456789012"
            }
        }
    }
}
```

#### YAML<a name="aws-properties-ec2-security-group-ingress--examples--Allow_Traffic_from_a_Security_Group_in_a_Peered_VPC--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  TargetSG:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      VpcId: vpc-1a2b3c4d
      GroupDescription: Security group allowing ingress for security scanners
  InboundRule:
    Type: 'AWS::EC2::SecurityGroupIngress'
    Properties:
      GroupId: !GetAtt TargetSG.GroupId
      IpProtocol: tcp
      FromPort: '80'
      ToPort: '80'
      SourceSecurityGroupId: sg-12345678
      SourceSecurityGroupOwnerId: '123456789012'
```

### VPC Security Groups with Egress and Ingress Rules<a name="aws-properties-ec2-security-group-ingress--examples--VPC_Security_Groups_with_Egress_and_Ingress_Rules"></a>

In some cases, you might have an originating \(source\) security group to which you want to add an outbound rule that allows traffic to a destination \(target\) security group\. The target security group also needs an inbound rule that allows traffic from the source security group\. Note that you cannot use the Ref function to specify the outbound and inbound rules for each security group\. Doing so creates a circular dependency; you cannot have two resources that depend on each other\. Instead, use the egress and ingress resources to declare these outbound and inbound rules, as shown in the following template example\. 

#### JSON<a name="aws-properties-ec2-security-group-ingress--examples--VPC_Security_Groups_with_Egress_and_Ingress_Rules--json"></a>

```
"Resources": {
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
}
```

#### YAML<a name="aws-properties-ec2-security-group-ingress--examples--VPC_Security_Groups_with_Egress_and_Ingress_Rules--yaml"></a>

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

### Allow Ping Requests<a name="aws-properties-ec2-security-group-ingress--examples--Allow__Ping_Requests"></a>

To allow ping requests, add the ICMP protocol type and specify 8 \(echo request\) for the ICMP type and either 0 or \-1 \(all\) for the ICMP code\. 

#### JSON<a name="aws-properties-ec2-security-group-ingress--examples--Allow__Ping_Requests--json"></a>

```
"SGPing" : {
  "Type" : "AWS::EC2::SecurityGroup",
  "DependsOn": "VPC",
  "Properties" : {
     "GroupDescription" : "SG to test ping",
     "VpcId" : {"Ref" : "VPC"},
     "SecurityGroupIngress" : [ 
        { "IpProtocol" : "tcp", "FromPort" : 22, "ToPort" : 22, "CidrIp" : "10.0.0.0/24" },
        { "IpProtocol" : "icmp", "FromPort" : 8, "ToPort" : -1, "CidrIp" : "10.0.0.0/24" }
      ]
   }
}
```

#### YAML<a name="aws-properties-ec2-security-group-ingress--examples--Allow__Ping_Requests--yaml"></a>

```
SGPing:
   Type: AWS::EC2::SecurityGroup
    DependsOn: VPC
    Properties:
      GroupDescription: SG to test ping
      VpcId:
         Ref: VPC
      SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: 22
        ToPort: 22
        CidrIp: 10.0.0.0/24
      - IpProtocol: icmp
        FromPort: 8
        ToPort: -1
        CidrIp: 10.0.0.0/24
```