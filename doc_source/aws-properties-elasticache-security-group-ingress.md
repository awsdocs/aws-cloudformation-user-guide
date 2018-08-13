# AWS::ElastiCache::SecurityGroupIngress<a name="aws-properties-elasticache-security-group-ingress"></a>

The AWS::ElastiCache::SecurityGroupIngress type authorizes ingress to a cache security group from hosts in specified Amazon EC2 security groups\. For more information about ElastiCache security group ingress, go to [AuthorizeCacheSecurityGroupIngress](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_AuthorizeCacheSecurityGroupIngress.html) in the *Amazon ElastiCache API Reference Guide*\.

**Topics**
+ [Syntax](#aws-resource-elasticache-securitygroupingress-syntax)
+ [Properties](#w3ab2c21c10d603b9)

## Syntax<a name="aws-resource-elasticache-securitygroupingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-securitygroupingress-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::SecurityGroupIngress",
  "Properties" :
  {
    "[CacheSecurityGroupName](#cfn-elasticache-securitygroupingress-cachesecuritygroupname)" : String,
    "[EC2SecurityGroupName](#cfn-elasticache-securitygroupingress-ec2securitygroupname)" : String,
    "[EC2SecurityGroupOwnerId](#cfn-elasticache-securitygroupingress-ec2securitygroupownerid)" : String
  }
}
```

### YAML<a name="aws-resource-elasticache-securitygroupingress-syntax.yaml"></a>

```
Type: "AWS::ElastiCache::SecurityGroupIngress"
Properties:
  [CacheSecurityGroupName](#cfn-elasticache-securitygroupingress-cachesecuritygroupname): String
  [EC2SecurityGroupName](#cfn-elasticache-securitygroupingress-ec2securitygroupname): String
  [EC2SecurityGroupOwnerId](#cfn-elasticache-securitygroupingress-ec2securitygroupownerid): String
```

## Properties<a name="w3ab2c21c10d603b9"></a>

`CacheSecurityGroupName`  <a name="cfn-elasticache-securitygroupingress-cachesecuritygroupname"></a>
The name of the Cache Security Group to authorize\.  
*Type*: String  
*Required*: Yes  
*Update requires*: Updates are not supported\.

`EC2SecurityGroupName`  <a name="cfn-elasticache-securitygroupingress-ec2securitygroupname"></a>
Name of the EC2 Security Group to include in the authorization\.  
*Type*: String  
*Required*: Yes  
*Update requires*: Updates are not supported\.

`EC2SecurityGroupOwnerId`  <a name="cfn-elasticache-securitygroupingress-ec2securitygroupownerid"></a>
Specifies the AWS Account ID of the owner of the EC2 security group specified in the EC2SecurityGroupName property\. The AWS access key ID is not an acceptable value\.  
*Type*: String  
*Required*: No  
*Update requires*: Updates are not supported\.