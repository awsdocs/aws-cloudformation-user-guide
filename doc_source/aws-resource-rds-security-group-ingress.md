# AWS::RDS::DBSecurityGroupIngress<a name="aws-resource-rds-security-group-ingress"></a>

The AWS::RDS::DBSecurityGroupIngress type enables ingress to a DBSecurityGroup using one of two forms of authorization\. First, EC2 or VPC security groups can be added to the DBSecurityGroup if the application using the database is running on EC2 or VPC instances\. Second, IP ranges are available if the application accessing your database is running on the Internet\. For more information about DB security groups, see [Working with DB security groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithSecurityGroups.html)

This type supports updates\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

For details about the settings for DB security group ingress, see [AuthorizeDBSecurityGroupIngress](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_AuthorizeDBSecurityGroupIngress.html)\.

**Topics**
+ [Syntax](#aws-resource-rds-dbsecuritygroupingress-syntax)
+ [Properties](#cfn-rds-securitygroup-ingress-properties)
+ [Return Values](#w3ab2c21c10d972c15)
+ [See Also](#w3ab2c21c10d972c17)

## Syntax<a name="aws-resource-rds-dbsecuritygroupingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbsecuritygroupingress-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBSecurityGroupIngress",
  "Properties" : {
   "[CIDRIP](#cfn-rds-securitygroup-ingress-cidrip)": String,
   "[DBSecurityGroupName](#cfn-rds-securitygroup-ingress-dbsecuritygroupname)": String,
   "[EC2SecurityGroupId](#cfn-rds-securitygroup-ingress-ec2securitygroupid)": String,
   "[EC2SecurityGroupName](#cfn-rds-securitygroup-ingress-ec2securitygroupname)": String,
   "[EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ingress-ec2securitygroupownerid)": String
}
```

### YAML<a name="aws-resource-rds-dbsecuritygroupingress-syntax.yaml"></a>

```
Type: "AWS::RDS::DBSecurityGroupIngress"
Properties:  
  [CIDRIP](#cfn-rds-securitygroup-ingress-cidrip): String
  [DBSecurityGroupName](#cfn-rds-securitygroup-ingress-dbsecuritygroupname): String
  [EC2SecurityGroupId](#cfn-rds-securitygroup-ingress-ec2securitygroupid): String
  [EC2SecurityGroupName](#cfn-rds-securitygroup-ingress-ec2securitygroupname): String
  [EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ingress-ec2securitygroupownerid): String
```

## Properties<a name="cfn-rds-securitygroup-ingress-properties"></a>

`CIDRIP`  <a name="cfn-rds-securitygroup-ingress-cidrip"></a>
The IP range to authorize\.  
For an overview of CIDR ranges, go to the [Wikipedia Tutorial](http://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DBSecurityGroupName`  <a name="cfn-rds-securitygroup-ingress-dbsecuritygroupname"></a>
The name \(ARN\) of the [AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md) to which this ingress will be added\.  
*Type*: String  
*Required*: Yes  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EC2SecurityGroupId`  <a name="cfn-rds-securitygroup-ingress-ec2securitygroupid"></a>
The ID of the VPC or EC2 security group to authorize\.  
For VPC DB security groups, use EC2SecurityGroupId\. For EC2 security groups, use EC2SecurityGroupOwnerId and either EC2SecurityGroupName or EC2SecurityGroupId\.  
*Type*: String  
*Required*: No  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EC2SecurityGroupName`  <a name="cfn-rds-securitygroup-ingress-ec2securitygroupname"></a>
The name of the EC2 security group to authorize\.  
For VPC DB security groups, use EC2SecurityGroupId\. For EC2 security groups, use EC2SecurityGroupOwnerId and either EC2SecurityGroupName or EC2SecurityGroupId\.  
*Type*: String  
*Required*: No  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EC2SecurityGroupOwnerId`  <a name="cfn-rds-securitygroup-ingress-ec2securitygroupownerid"></a>
The AWS Account Number of the owner of the EC2 security group specified in the EC2SecurityGroupName parameter\. The AWS Access Key ID is not an acceptable value\.  
For VPC DB security groups, use EC2SecurityGroupId\. For EC2 security groups, use EC2SecurityGroupOwnerId and either EC2SecurityGroupName or EC2SecurityGroupId\.  
*Type*: String  
*Required*: No  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d972c15"></a>

### Ref<a name="w3ab2c21c10d972c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="w3ab2c21c10d972c17"></a>
+ [AuthorizeDBSecurityGroupIngress](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_AuthorizeDBSecurityGroupIngress.html) in the *Amazon Relational Database Service API Reference*