# AWS::RDS::DBSecurityGroup<a name="aws-properties-rds-security-group"></a>

The `AWS::RDS::DBSecurityGroup` resource creates or updates an Amazon RDS DB security group\.

**Note**  
DB security groups are a part of the EC2\-Classic Platform and as such are not supported in all regions\. It is advised to use the `AWS::EC2::SecurityGroup` resource in those regions instead\. To determine which platform you are on, see [Determining Whether You Are Using the EC2\-VPC or EC2\-Classic Platform](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.FindDefaultVPC.html)\. For more information on the `AWS::EC2::SecurityGroup`, see the documentation for [EC2 security groups](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html)\.

## Syntax<a name="aws-properties-rds-security-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-security-group-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBSecurityGroup",
  "Properties" : {
      "[DBSecurityGroupIngress](#cfn-rds-dbsecuritygroup-dbsecuritygroupingress)" : [ Ingress, ... ],
      "[EC2VpcId](#cfn-rds-dbsecuritygroup-ec2vpcid)" : String,
      "[GroupDescription](#cfn-rds-dbsecuritygroup-groupdescription)" : String,
      "[Tags](#cfn-rds-dbsecuritygroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-properties-rds-security-group-syntax.yaml"></a>

```
Type: AWS::RDS::DBSecurityGroup
Properties: 
  [DBSecurityGroupIngress](#cfn-rds-dbsecuritygroup-dbsecuritygroupingress): 
    - Ingress
  [EC2VpcId](#cfn-rds-dbsecuritygroup-ec2vpcid): String
  [GroupDescription](#cfn-rds-dbsecuritygroup-groupdescription): String
  [Tags](#cfn-rds-dbsecuritygroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-rds-security-group-properties"></a>

`DBSecurityGroupIngress`  <a name="cfn-rds-dbsecuritygroup-dbsecuritygroupingress"></a>
Ingress rules to be applied to the DB security group\.  
*Required*: Yes  
*Type*: List of [Ingress](aws-properties-rds-security-group-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2VpcId`  <a name="cfn-rds-dbsecuritygroup-ec2vpcid"></a>
The identifier of an Amazon VPC\. This property indicates the VPC that this DB security group belongs to\.  
The `EC2VpcId` property is for backward compatibility with older regions, and is no longer recommended for providing security information to an RDS DB instance\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupDescription`  <a name="cfn-rds-dbsecuritygroup-groupdescription"></a>
Provides the description of the DB Security Group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rds-dbsecuritygroup-tags"></a>
Tags to assign to the DB security group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-rds-security-group-return-values"></a>

### Ref<a name="aws-properties-rds-security-group-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB security group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-rds-security-group--examples"></a>



### Creating a single VPC security group<a name="aws-properties-rds-security-group--examples--Creating_a_single_VPC_security_group"></a>

The following example creates a single VPC security group, referred to by `EC2SecurityGroupName`\. 

#### JSON<a name="aws-properties-rds-security-group--examples--Creating_a_single_VPC_security_group--json"></a>

```
{
    "Resources": {
        "DBinstance": {
            "Type": "AWS::RDS::DBInstance",
            "Properties": {
                "DBSecurityGroups": [
                    {
                        "Ref": "DbSecurityByEC2SecurityGroup"
                    }
                ],
                "AllocatedStorage": "5",
                "DBInstanceClass": "db.t3.small",
                "Engine": "MySQL",
                "MasterUsername": "YourName",
                "MasterUserPassword": "YourPassword"
            },
            "DeletionPolicy": "Snapshot"
        },
        "DbSecurityByEC2SecurityGroup": {
            "Type": "AWS::RDS::DBSecurityGroup",
            "Properties": {
                "GroupDescription": "Ingress for Amazon EC2 security group",
                "DBSecurityGroupIngress": [
                    {
                        "EC2SecurityGroupId": "sg-b0ff1111",
                        "EC2SecurityGroupOwnerId": "111122223333"
                    },
                    {
                        "EC2SecurityGroupId": "sg-ffd722222",
                        "EC2SecurityGroupOwnerId": "111122223333"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-properties-rds-security-group--examples--Creating_a_single_VPC_security_group--yaml"></a>

```
Resources: 
  DBinstance: 
    Type: AWS::RDS::DBInstance
    Properties: 
      DBSecurityGroups: 
        - 
          Ref: "DbSecurityByEC2SecurityGroup"
      AllocatedStorage: "5"
      DBInstanceClass: "db.t3.small"
      Engine: "MySQL"
      MasterUsername: "YourName"
      MasterUserPassword: "YourPassword"
    DeletionPolicy: "Snapshot"
  DbSecurityByEC2SecurityGroup: 
    Type: AWS::RDS::DBSecurityGroup
    Properties: 
      GroupDescription: "Ingress for Amazon EC2 security group"
      DBSecurityGroupIngress: 
        - 
          EC2SecurityGroupId: "sg-b0ff1111"
          EC2SecurityGroupOwnerId: "111122223333"
        - 
          EC2SecurityGroupId: "sg-ffd722222"
          EC2SecurityGroupOwnerId: "111122223333"
```

### Multiple VPC security groups<a name="aws-properties-rds-security-group--examples--Multiple_VPC_security_groups"></a>

The following example creates or updates multiple VPC security groups\. 

#### JSON<a name="aws-properties-rds-security-group--examples--Multiple_VPC_security_groups--json"></a>

```
"DBSecurityGroup": {
   "Type": "AWS::RDS::DBSecurityGroup",
   "Properties": {
      "EC2VpcId" : { "Ref" : "VpcId" },
      "DBSecurityGroupIngress": [
         {"EC2SecurityGroupName": { "Ref": "WebServerSecurityGroup"}}
      ],
      "GroupDescription": "Frontend Access"
   }
}
```

#### YAML<a name="aws-properties-rds-security-group--examples--Multiple_VPC_security_groups--yaml"></a>

```
DBSecurityGroup: 
  Type: AWS::RDS::DBSecurityGroup
  Properties: 
    EC2VpcId: 
      Ref: "VpcId"
    DBSecurityGroupIngress: 
      - 
        EC2SecurityGroupName: 
          Ref: "WebServerSecurityGroup"
    GroupDescription: "Frontend Access"
```