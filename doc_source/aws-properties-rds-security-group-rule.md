# Amazon RDS Security Group Rule<a name="aws-properties-rds-security-group-rule"></a>

The Amazon RDS security group rule is an embedded property of the [AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md) type\.

## Syntax<a name="w3ab2c21c14e1639b5"></a>

### JSON<a name="aws-properties-rds-security-group-rule-syntax.json"></a>

```
{
  "[CIDRIP](#cfn-rds-securitygroup-cidrip)": String,
  "[EC2SecurityGroupId](#cfn-rds-securitygroup-ec2securitygroupid)": String,
  "[EC2SecurityGroupName](#cfn-rds-securitygroup-ec2securitygroupname)": String,
  "[EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ec2securitygroupownerid)": String
}
```

### YAML<a name="aws-properties-rds-security-group-rule-syntax.yaml"></a>

```
[CIDRIP](#cfn-rds-securitygroup-cidrip): String
[EC2SecurityGroupId](#cfn-rds-securitygroup-ec2securitygroupid): String
[EC2SecurityGroupName](#cfn-rds-securitygroup-ec2securitygroupname): String
[EC2SecurityGroupOwnerId](#cfn-rds-securitygroup-ec2securitygroupownerid): String
```

## Properties<a name="cfn-rds-securitygroup-properties"></a>

`CIDRIP`  <a name="cfn-rds-securitygroup-cidrip"></a>
The IP range to authorize\.  
For an overview of CIDR ranges, go to the [Wikipedia Tutorial](http://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\.  
*Type*: String  
*Required*: No  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EC2SecurityGroupId`  <a name="cfn-rds-securitygroup-ec2securitygroupid"></a>
Id of the VPC or EC2 Security Group to authorize\.  
For VPC DB Security Groups, use EC2SecurityGroupId\. For EC2 Security Groups, use EC2SecurityGroupOwnerId and either EC2SecurityGroupName or EC2SecurityGroupId\.  
*Type*: String  
*Required*: No  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EC2SecurityGroupName`  <a name="cfn-rds-securitygroup-ec2securitygroupname"></a>
Name of the EC2 Security Group to authorize\.  
For VPC DB Security Groups, use EC2SecurityGroupId\. For EC2 Security Groups, use EC2SecurityGroupOwnerId and either EC2SecurityGroupName or EC2SecurityGroupId\.  
*Type*: String  
*Required*: No  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EC2SecurityGroupOwnerId`  <a name="cfn-rds-securitygroup-ec2securitygroupownerid"></a>
AWS Account Number of the owner of the EC2 Security Group specified in the EC2SecurityGroupName parameter\. The AWS Access Key ID is not an acceptable value\.  
For VPC DB Security Groups, use EC2SecurityGroupId\. For EC2 Security Groups, use EC2SecurityGroupOwnerId and either EC2SecurityGroupName or EC2SecurityGroupId\.  
*Type*: String  
*Required*: No  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)