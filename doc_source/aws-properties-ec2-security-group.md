# AWS::EC2::SecurityGroup<a name="aws-properties-ec2-security-group"></a>

Specifies a security group\. To create a security group, use the [VpcId](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html#cfn-ec2-securitygroup-vpcid) property to specify the VPC for which to create the security group\.

This type supports updates\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

**Important**  
If you want to cross\-reference two security groups in the ingress and egress rules of those security groups, use the [AWS::EC2::SecurityGroupEgress](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-security-group-egress.html) and [AWS::EC2::SecurityGroupIngress](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-security-group-ingress.html) resources to define your rules\. Do not use the embedded ingress and egress rules in the `AWS::EC2::SecurityGroup`\. Doing so creates a circular dependency, which CloudFormation doesn't allow\.

## Syntax<a name="aws-properties-ec2-security-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-security-group-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SecurityGroup",
  "Properties" : {
      "[GroupDescription](#cfn-ec2-securitygroup-groupdescription)" : String,
      "[GroupName](#cfn-ec2-securitygroup-groupname)" : String,
      "[SecurityGroupEgress](#cfn-ec2-securitygroup-securitygroupegress)" : [ Egress, ... ],
      "[SecurityGroupIngress](#cfn-ec2-securitygroup-securitygroupingress)" : [ Ingress, ... ],
      "[Tags](#cfn-ec2-securitygroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-ec2-securitygroup-vpcid)" : String
    }
}
```

### YAML<a name="aws-properties-ec2-security-group-syntax.yaml"></a>

```
Type: AWS::EC2::SecurityGroup
Properties: 
  [GroupDescription](#cfn-ec2-securitygroup-groupdescription): String
  [GroupName](#cfn-ec2-securitygroup-groupname): String
  [SecurityGroupEgress](#cfn-ec2-securitygroup-securitygroupegress): 
    - Egress
  [SecurityGroupIngress](#cfn-ec2-securitygroup-securitygroupingress): 
    - Ingress
  [Tags](#cfn-ec2-securitygroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-ec2-securitygroup-vpcid): String
```

## Properties<a name="aws-properties-ec2-security-group-properties"></a>

`GroupDescription`  <a name="cfn-ec2-securitygroup-groupdescription"></a>
A description for the security group\. This is informational only\.  
Constraints: Up to 255 characters in length  
Constraints for EC2\-Classic: ASCII characters  
Constraints for EC2\-VPC: a\-z, A\-Z, 0\-9, spaces, and \.\_\-:/\(\)\#,@\[\]\+=&;\{\}\!$\*  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupName`  <a name="cfn-ec2-securitygroup-groupname"></a>
The name of the security group\.  
Constraints: Up to 255 characters in length\. Cannot start with `sg-`\.  
Constraints for EC2\-Classic: ASCII characters  
Constraints for EC2\-VPC: a\-z, A\-Z, 0\-9, spaces, and \.\_\-:/\(\)\#,@\[\]\+=&;\{\}\!$\*  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupEgress`  <a name="cfn-ec2-securitygroup-securitygroupegress"></a>
\[VPC only\] The outbound rules associated with the security group\. There is a short interruption during which you cannot connect to the security group\.  
*Required*: No  
*Type*: List of [Egress](aws-properties-ec2-security-group-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIngress`  <a name="cfn-ec2-securitygroup-securitygroupingress"></a>
The inbound rules associated with the security group\. There is a short interruption during which you cannot connect to the security group\.  
*Required*: No  
*Type*: List of [Ingress](aws-properties-ec2-security-group-rule-1.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-securitygroup-tags"></a>
Any tags assigned to the security group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-securitygroup-vpcid"></a>
\[VPC only\] The ID of the VPC for the security group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-properties-ec2-security-group-return-values"></a>

### Ref<a name="aws-properties-ec2-security-group-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID\. For security groups that were created without specifying a VPC \(EC2\-Classic or a default VPC\), `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-ec2-security-group-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-ec2-security-group-return-values-fn--getatt-fn--getatt"></a>

`GroupId`  <a name="GroupId-fn::getatt"></a>
The group ID of the specified security group, such as `sg-94b3a1f6`\.

`VpcId`  <a name="VpcId-fn::getatt"></a>
The physical ID of the VPC\. You can obtain the physical ID by using a reference to an [AWS::EC2::VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc.html), such as: `{ "Ref" : "myVPC" }`\.

## Examples<a name="aws-properties-ec2-security-group--examples"></a>



### Define Basic Ingress and Egress Rules<a name="aws-properties-ec2-security-group--examples--Define_Basic_Ingress_and_Egress_Rules"></a>

The following example specifies a security group with an ingress and egress rule\. 

#### JSON<a name="aws-properties-ec2-security-group--examples--Define_Basic_Ingress_and_Egress_Rules--json"></a>

```
"InstanceSecurityGroup" : {
   "Type" : "AWS::EC2::SecurityGroup",
   "Properties" : {
      "GroupDescription" : "Allow http to client host",
      "VpcId" : {"Ref" : "myVPC"},
      "SecurityGroupIngress" : [{
         "IpProtocol" : "tcp",
         "FromPort" : 80,
         "ToPort" : 80,
         "CidrIp" : "0.0.0.0/0"
      }],
      "SecurityGroupEgress" : [{
         "IpProtocol" : "tcp",
         "FromPort" : 80,
         "ToPort" : 80,
         "CidrIp" : "0.0.0.0/0"
      }]
   }
}
```

#### YAML<a name="aws-properties-ec2-security-group--examples--Define_Basic_Ingress_and_Egress_Rules--yaml"></a>

```
InstanceSecurityGroup:
  Type: AWS::EC2::SecurityGroup
  Properties:
      GroupDescription: Allow http to client host
      VpcId:
         Ref: myVPC
      SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: 80
        ToPort: 80
        CidrIp: 0.0.0.0/0
      SecurityGroupEgress:
      - IpProtocol: tcp
        FromPort: 80
        ToPort: 80
        CidrIp: 0.0.0.0/0
```

### Remove Default Rule<a name="aws-properties-ec2-security-group--examples--Remove_Default_Rule"></a>

When you specify a VPC security group, Amazon EC2 creates a default egress rule that allows egress traffic on all ports and IP protocols to any location\. The default rule is removed only when you specify one or more egress rules\. If you want to remove the default rule and limit egress traffic to just the localhost \(127\.0\.0\.1/32\), use the following example\. 

#### JSON<a name="aws-properties-ec2-security-group--examples--Remove_Default_Rule--json"></a>

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

#### YAML<a name="aws-properties-ec2-security-group--examples--Remove_Default_Rule--yaml"></a>

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

## See also<a name="aws-properties-ec2-security-group--seealso"></a>
+  [Security Groups for Your VPC](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) in the *Amazon VPC User Guide*
+  [EC2\-Classic](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-classic-platform.html) in the *Amazon EC2 User Guide for Linux Instances* for information about accounts that support EC2\-Classic security groups
+  [Amazon EC2 Security Groups for Linux Instances ](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html) in the *Amazon EC2 User Guide for Linux Instances*

