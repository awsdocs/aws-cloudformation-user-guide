# AWS::ElastiCache::SecurityGroup<a name="aws-properties-elasticache-security-group"></a>

The `AWS::ElastiCache::SecurityGroup` resource creates a cache security group\. For more information about cache security groups, go to [CacheSecurityGroups](https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/VPCs.html) in the *Amazon ElastiCache User Guide* or go to [CreateCacheSecurityGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheSecurityGroup.html) in the *Amazon ElastiCache API Reference Guide*\. 

For more information, see [CreateCacheSubnetGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheSubnetGroup.html)\.

**Note**  
Updates are not supported\.

## Syntax<a name="aws-properties-elasticache-security-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-security-group-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::SecurityGroup",
  "Properties" : {
      "[Description](#cfn-elasticache-securitygroup-description)" : String
    }
}
```

### YAML<a name="aws-properties-elasticache-security-group-syntax.yaml"></a>

```
Type: AWS::ElastiCache::SecurityGroup
Properties: 
  [Description](#cfn-elasticache-securitygroup-description): String
```

## Properties<a name="aws-properties-elasticache-security-group-properties"></a>

`Description`  <a name="cfn-elasticache-securitygroup-description"></a>
A description for the cache security group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-elasticache-security-group-return-values"></a>

### Ref<a name="aws-properties-elasticache-security-group-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.