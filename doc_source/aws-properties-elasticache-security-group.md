# AWS::ElastiCache::SecurityGroup<a name="aws-properties-elasticache-security-group"></a>

The `AWS::ElastiCache::SecurityGroup` resource creates a cache security group\. For more information about cache security groups, go to [Cache Security Groups](http://docs.aws.amazon.com/AmazonElastiCache/latest/UserGuide/CacheSecurityGroup.html) in the *Amazon ElastiCache User Guide* or go to [CreateCacheSecurityGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheSecurityGroup.html) in the *Amazon ElastiCache API Reference Guide*\.

To create an ElastiCache cluster in a VPC, use the [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md) resource\. For more information, see the `VpcSecurityGroupIds` property in the [AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md) resource\.

**Topics**
+ [Syntax](#aws-resource-elasticache-securitygroup-syntax)
+ [Properties](#w3ab2c21c10d598c11)
+ [Return Values](#w3ab2c21c10d598c13)

## Syntax<a name="aws-resource-elasticache-securitygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-securitygroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::SecurityGroup",
  "Properties" :
  {
    "[Description](#cfn-elasticache-securitygroup-description)" : String
  }
}
```

### YAML<a name="aws-resource-elasticache-securitygroup-syntax.yaml"></a>

```
Type: "AWS::ElastiCache::SecurityGroup"
Properties:
  [Description](#cfn-elasticache-securitygroup-description): String
```

## Properties<a name="w3ab2c21c10d598c11"></a>

`Description`  <a name="cfn-elasticache-securitygroup-description"></a>
A description for the cache security group\.  
*Type*: String  
*Required*: No  
*Update requires*: Updates are not supported\.

## Return Values<a name="w3ab2c21c10d598c13"></a>

### Ref<a name="w3ab2c21c10d598c13b2"></a>

When you specify the `AWS::ElastiCache::SecurityGroup` resource as an argument to the `Ref` function, AWS CloudFormation returns the `CacheSecurityGroupName` property of the cache security group\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.