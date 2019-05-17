# AWS::RDS::DBSecurityGroup Ingress<a name="aws-properties-rds-security-group-rule"></a>

The `Ingress` property type specifies an individual ingress rule within an `AWS::RDS::DBSecurityGroup` resource\.

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
 Id of the EC2 Security Group to authorize\. For VPC DB Security Groups, `EC2SecurityGroupId` must be provided\. Otherwise, EC2SecurityGroupOwnerId and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EC2SecurityGroupName`  <a name="cfn-rds-securitygroup-ec2securitygroupname"></a>
 Name of the EC2 Security Group to authorize\. For VPC DB Security Groups, `EC2SecurityGroupId` must be provided\. Otherwise, EC2SecurityGroupOwnerId and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EC2SecurityGroupOwnerId`  <a name="cfn-rds-securitygroup-ec2securitygroupownerid"></a>
 AWS Account Number of the owner of the EC2 Security Group specified in the EC2SecurityGroupName parameter\. The AWS Access Key ID is not an acceptable value\. For VPC DB Security Groups, `EC2SecurityGroupId` must be provided\. Otherwise, EC2SecurityGroupOwnerId and either `EC2SecurityGroupName` or `EC2SecurityGroupId` must be provided\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)