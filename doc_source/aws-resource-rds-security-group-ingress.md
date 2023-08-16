# AWS::RDS::DBSecurityGroupIngress<a name="aws-resource-rds-security-group-ingress"></a>

The `AWS::RDS::DBSecurityGroupIngress` resource enables ingress to a DB security group using one of two forms of authorization\. First, you can add EC2 or VPC security groups to the DB security group if the application using the database is running on EC2 or VPC instances\. Second, IP ranges are available if the application accessing your database is running on the Internet\.

This type supports updates\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

For details about the settings for DB security group ingress, see [AuthorizeDBSecurityGroupIngress](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_AuthorizeDBSecurityGroupIngress.html)\.

**Note**  
EC2\-Classic was retired on August 15, 2022\. If you haven't migrated from EC2\-Classic to a VPC, we recommend that you migrate as soon as possible\. For more information, see [Migrate from EC2\-Classic to a VPC](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/vpc-migrate.html) in the *Amazon EC2 User Guide*, the blog [EC2\-Classic Networking is Retiring – Here’s How to Prepare](http://aws.amazon.com/blogs/aws/ec2-classic-is-retiring-heres-how-to-prepare/), and [Moving a DB instance not in a VPC into a VPC](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.Non-VPC2VPC.html) in the *Amazon RDS User Guide*\.

## Syntax<a name="aws-resource-rds-security-group-ingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-security-group-ingress-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBSecurityGroupIngress",
  "Properties" : {
      "[CIDRIP](#cfn-rds-securitygroup-ingress-cidrip)" : String,
      "[DBSecurityGroupName](#cfn-rds-securitygroup-ingress-dbsecuritygroupname)" : String,
      "[EC2SecurityGroupId](#cfn-rds-securitygroup-ingress-ec2securitygroupid)" : String,
      "[EC2SecurityGroupName](#cfn-rds-securitygroup-ingress-ec2securitygroupname)" : String,
      "[EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ingress-ec2securitygroupownerid)" : String
    }
}
```

### YAML<a name="aws-resource-rds-security-group-ingress-syntax.yaml"></a>

```
Type: AWS::RDS::DBSecurityGroupIngress
Properties: 
  [CIDRIP](#cfn-rds-securitygroup-ingress-cidrip): String
  [DBSecurityGroupName](#cfn-rds-securitygroup-ingress-dbsecuritygroupname): String
  [EC2SecurityGroupId](#cfn-rds-securitygroup-ingress-ec2securitygroupid): String
  [EC2SecurityGroupName](#cfn-rds-securitygroup-ingress-ec2securitygroupname): String
  [EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ingress-ec2securitygroupownerid): String
```

## Properties<a name="aws-resource-rds-security-group-ingress-properties"></a>

`CIDRIP`  <a name="cfn-rds-securitygroup-ingress-cidrip"></a>
The IP range to authorize\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSecurityGroupName`  <a name="cfn-rds-securitygroup-ingress-dbsecuritygroupname"></a>
The name of the DB security group to add authorization to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2SecurityGroupId`  <a name="cfn-rds-securitygroup-ingress-ec2securitygroupid"></a>
Id of the EC2 security group to authorize\. For VPC DB security groups, `EC2SecurityGroupId` must be provided\. Otherwise, `EC2SecurityGroupOwnerId` and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2SecurityGroupName`  <a name="cfn-rds-securitygroup-ingress-ec2securitygroupname"></a>
Name of the EC2 security group to authorize\. For VPC DB security groups, `EC2SecurityGroupId` must be provided\. Otherwise, `EC2SecurityGroupOwnerId` and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2SecurityGroupOwnerId`  <a name="cfn-rds-securitygroup-ingress-ec2securitygroupownerid"></a>
 AWS account number of the owner of the EC2 security group specified in the `EC2SecurityGroupName` parameter\. The AWS access key ID isn't an acceptable value\. For VPC DB security groups, `EC2SecurityGroupId` must be provided\. Otherwise, `EC2SecurityGroupOwnerId` and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-security-group-ingress-return-values"></a>

### Ref<a name="aws-resource-rds-security-group-ingress-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the DB security group that this ingress rule is associated with\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.