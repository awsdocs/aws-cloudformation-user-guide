# AWS::RDS::DBSecurityGroup Ingress<a name="aws-properties-rds-security-group-rule"></a>

The `Ingress` property type specifies an individual ingress rule within an `AWS::RDS::DBSecurityGroup` resource\.

**Note**  
EC2\-Classic was retired on August 15, 2022\. If you haven't migrated from EC2\-Classic to a VPC, we recommend that you migrate as soon as possible\. For more information, see [Migrate from EC2\-Classic to a VPC](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/vpc-migrate.html) in the *Amazon EC2 User Guide*, the blog [EC2\-Classic Networking is Retiring – Here’s How to Prepare](http://aws.amazon.com/blogs/aws/ec2-classic-is-retiring-heres-how-to-prepare/), and [Moving a DB instance not in a VPC into a VPC](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.Non-VPC2VPC.html) in the *Amazon RDS User Guide*\.

## Syntax<a name="aws-properties-rds-security-group-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-security-group-rule-syntax.json"></a>

```
{
  "[CIDRIP](#cfn-rds-securitygroup-cidrip)" : String,
  "[EC2SecurityGroupId](#cfn-rds-securitygroup-ec2securitygroupid)" : String,
  "[EC2SecurityGroupName](#cfn-rds-securitygroup-ec2securitygroupname)" : String,
  "[EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ec2securitygroupownerid)" : String
}
```

### YAML<a name="aws-properties-rds-security-group-rule-syntax.yaml"></a>

```
  [CIDRIP](#cfn-rds-securitygroup-cidrip): String
  [EC2SecurityGroupId](#cfn-rds-securitygroup-ec2securitygroupid): String
  [EC2SecurityGroupName](#cfn-rds-securitygroup-ec2securitygroupname): String
  [EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ec2securitygroupownerid): String
```

## Properties<a name="aws-properties-rds-security-group-rule-properties"></a>

`CIDRIP`  <a name="cfn-rds-securitygroup-cidrip"></a>
The IP range to authorize\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2SecurityGroupId`  <a name="cfn-rds-securitygroup-ec2securitygroupid"></a>
Id of the EC2 security group to authorize\. For VPC DB security groups, `EC2SecurityGroupId` must be provided\. Otherwise, `EC2SecurityGroupOwnerId` and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EC2SecurityGroupName`  <a name="cfn-rds-securitygroup-ec2securitygroupname"></a>
Name of the EC2 security group to authorize\. For VPC DB security groups, `EC2SecurityGroupId` must be provided\. Otherwise, `EC2SecurityGroupOwnerId` and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EC2SecurityGroupOwnerId`  <a name="cfn-rds-securitygroup-ec2securitygroupownerid"></a>
 AWS account number of the owner of the EC2 security group specified in the `EC2SecurityGroupName` parameter\. The AWS access key ID isn't an acceptable value\. For VPC DB security groups, `EC2SecurityGroupId` must be provided\. Otherwise, `EC2SecurityGroupOwnerId` and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)