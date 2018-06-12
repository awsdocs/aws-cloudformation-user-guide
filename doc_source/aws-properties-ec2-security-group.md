# AWS::EC2::SecurityGroup<a name="aws-properties-ec2-security-group"></a>

Creates an Amazon EC2 security group\. To create a VPC security group, use the [VpcId](#cfn-ec2-securitygroup-vpcid) property\.

This type supports updates\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

**Important**  
If you want to cross\-reference two security groups in the ingress and egress rules of those security groups, use the [AWS::EC2::SecurityGroupEgress](aws-resource-ec2-security-group-egress.md) and [AWS::EC2::SecurityGroupIngress](aws-properties-ec2-security-group-ingress.md) resources to define your rules\. Do not use the embedded ingress and egress rules in the `AWS::EC2::SecurityGroup`\. Doing so creates a circular dependency, which AWS CloudFormation doesn't allow\.

**Topics**
+ [Syntax](#aws-resource-ec2-securitygroup-syntax)
+ [Properties](#w3ab2c21c10d465c13)
+ [Return Values](#w3ab2c21c10d465c15)
+ [Examples](#w3ab2c21c10d465c17)
+ [More Info](#w3ab2c21c10d465c19)

## Syntax<a name="aws-resource-ec2-securitygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-securitygroup-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SecurityGroup",
  "Properties" : {
     "[GroupName](#cfn-ec2-securitygroup-groupname)" : String,
     "[GroupDescription](#cfn-ec2-securitygroup-groupdescription)" : String,
     "[SecurityGroupEgress](#cfn-ec2-securitygroup-securitygroupegress)" : [ Security Group Rule, ... ],
     "[SecurityGroupIngress](#cfn-ec2-securitygroup-securitygroupingress)" : [ Security Group Rule, ... ],
     "[Tags](#cfn-ec2-securitygroup-tags)" :  [ Resource Tag, ... ],
     "[VpcId](#cfn-ec2-securitygroup-vpcid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-securitygroup-syntax.yaml"></a>

```
Type: "AWS::EC2::SecurityGroup"
Properties: 
  [GroupName](#cfn-ec2-securitygroup-groupname): String
  [GroupDescription](#cfn-ec2-securitygroup-groupdescription): String
  [SecurityGroupEgress](#cfn-ec2-securitygroup-securitygroupegress):
    - Security Group Rule
  [SecurityGroupIngress](#cfn-ec2-securitygroup-securitygroupingress):
    - Security Group Rule
  [Tags](#cfn-ec2-securitygroup-tags):
    - Resource Tag
  [VpcId](#cfn-ec2-securitygroup-vpcid): String
```

## Properties<a name="w3ab2c21c10d465c13"></a>

`GroupName`  <a name="cfn-ec2-securitygroup-groupname"></a>
The name of the security group\. For valid values, see the [GroupName](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSecurityGroup.html) parameter of the `CreateSecurityGroup` action in the *Amazon EC2 API Reference*\.  
If you don't specify a `GroupName`, AWS CloudFormation generates a unique physical ID and uses that ID for the group name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`GroupDescription`  <a name="cfn-ec2-securitygroup-groupdescription"></a>
A description of the security group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SecurityGroupEgress`  <a name="cfn-ec2-securitygroup-securitygroupegress"></a>
A list of Amazon EC2 security group egress rules\.  
*Required*: No  
*Type*: List of [EC2 Security Group Rule](aws-properties-ec2-security-group-rule.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SecurityGroupIngress`  <a name="cfn-ec2-securitygroup-securitygroupingress"></a>
A list of Amazon EC2 security group ingress rules\.  
*Required*: No  
*Type*: List of [EC2 Security Group Rule](aws-properties-ec2-security-group-rule.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-ec2-securitygroup-tags"></a>
The tags that you want to attach to the resource\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-securitygroup-vpcid"></a>
The physical ID of the VPC\. You can obtain the physical ID by using a reference to an [AWS::EC2::VPC](aws-resource-ec2-vpc.md), such as: `{ "Ref" : "myVPC" }`\.  
For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.  
*Required*: Yes, for VPC security groups without a default VPC  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
For more information about VPC security groups, see [Security Groups](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html) in the *Amazon VPC User Guide*\.

## Return Values<a name="w3ab2c21c10d465c15"></a>

### Ref<a name="w3ab2c21c10d465c15b2"></a>

When you specify an `AWS::EC2::SecurityGroup` type as an argument to the `Ref` function, AWS CloudFormation returns the security group name or the security group ID \(for EC2\-VPC security groups that are not in a default VPC\)\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d465c15b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`GroupId`  
The group ID of the specified security group, such as `sg-94b3a1f6`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d465c17"></a>

### Define Basic Ingress and Egress Rules<a name="w3ab2c21c10d465c17b2"></a>

The following example defines a security group with an ingress and egress rule\.

#### JSON<a name="aws-resource-ec2-securitygroup-example-1.json"></a>

```
"InstanceSecurityGroup" : {
   "Type" : "AWS::EC2::SecurityGroup",
   "Properties" : {
      "GroupDescription" : "Allow http to client host",
      "VpcId" : {"Ref" : "myVPC"},
      "SecurityGroupIngress" : [{
            "IpProtocol" : "tcp",
            "FromPort" : "80",
            "ToPort" : "80",
            "CidrIp" : "0.0.0.0/0"
         }],
      "SecurityGroupEgress" : [{
         "IpProtocol" : "tcp",
         "FromPort" : "80",
         "ToPort" : "80",
         "CidrIp" : "0.0.0.0/0"
      }]
   }
}
```

#### YAML<a name="aws-resource-ec2-securitygroup-example-1.yaml"></a>

```
InstanceSecurityGroup:
  Type: AWS::EC2::SecurityGroup
  Properties:
    GroupDescription: Allow http to client host
    VpcId:
      Ref: myVPC
    SecurityGroupIngress:
    - IpProtocol: tcp
      FromPort: '80'
      ToPort: '80'
      CidrIp: 0.0.0.0/0
    SecurityGroupEgress:
    - IpProtocol: tcp
      FromPort: '80'
      ToPort: '80'
      CidrIp: 0.0.0.0/0
```

### Remove Default Rule<a name="w3ab2c21c10d465c17b4"></a>

When you create a VPC security group, Amazon EC2 creates a default egress rule that allows egress traffic on all ports and IP protocols to any location\. The default rule is removed only when you specify one or more egress rules\. If you want to remove the default rule and limit egress traffic to just the localhost \(`127.0.0.1/32`\), use the following example\.

#### JSON<a name="aws-resource-ec2-securitygroup-example-2.json"></a>

```
"sgwithoutegress": {
  "Type": "AWS::EC2::SecurityGroup",
  "Properties": {
    "GroupDescription": "Limits security group egress traffic",
    "SecurityGroupEgress": [
      {
        "CidrIp": "127.0.0.1/32",
        "IpProtocol": "-1"
      }
    ],
    "VpcId": { "Ref": "myVPC"}
  }
}
```

#### YAML<a name="aws-resource-ec2-securitygroup-example-2.yaml"></a>

```
sgwithoutegress:
  Type: AWS::EC2::SecurityGroup
  Properties:
    GroupDescription: Limits security group egress traffic
    SecurityGroupEgress:
    - CidrIp: 127.0.0.1/32
      IpProtocol: "-1"
    VpcId:
      Ref: myVPC
```

## More Info<a name="w3ab2c21c10d465c19"></a>
+ [Using Security Groups](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html) in the *Amazon EC2 User Guide for Linux Instances*\.
+ [Security Groups](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html) in the *Amazon VPC User Guide*\.