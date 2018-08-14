# AWS::ElastiCache::SubnetGroup<a name="aws-properties-elasticache-subnetgroup"></a>

Creates a cache subnet group\. For more information about cache subnet groups, go to [Cache Subnet Groups](http://docs.aws.amazon.com/AmazonElastiCache/latest/UserGuide/CacheSubnetGroups.html) in the *Amazon ElastiCache User Guide* or go to [CreateCacheSubnetGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheSubnetGroup.html) in the *Amazon ElastiCache API Reference Guide*\.

**Topics**
+ [Syntax](#aws-resource-elasticache-subnetgroup-syntax)
+ [Properties](#w3ab2c21c10d610b9)
+ [Return Value](#w3ab2c21c10d610c11)
+ [Example](#w3ab2c21c10d610c13)

## Syntax<a name="aws-resource-elasticache-subnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-subnetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::SubnetGroup",
  "Properties" : {
    "[CacheSubnetGroupName](#cfn-elasticache-subnetgroup-cachesubnetgroupname)" : String,
    "[Description](#cfn-elasticache-subnetgroup-description)" : String,
    "[SubnetIds](#cfn-elasticache-subnetgroup-subnetids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-elasticache-subnetgroup-syntax.yaml"></a>

```
Type: "AWS::ElastiCache::SubnetGroup"
Properties:
  [CacheSubnetGroupName](#cfn-elasticache-subnetgroup-cachesubnetgroupname): String
  [Description](#cfn-elasticache-subnetgroup-description): String
  [SubnetIds](#cfn-elasticache-subnetgroup-subnetids):
    - String
```

## Properties<a name="w3ab2c21c10d610b9"></a>

`CacheSubnetGroupName`  <a name="cfn-elasticache-subnetgroup-cachesubnetgroupname"></a>
A name for the cache subnet group\. If you don't specify a name, AWS CloudFormation generates a unique physical ID\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-elasticache-subnetgroup-description"></a>
The description for the cache subnet group\.  
*Type*: String  
*Required*: Yes  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetIds`  <a name="cfn-elasticache-subnetgroup-subnetids"></a>
The Amazon EC2 subnet IDs for the cache subnet group\.  
*Type*: String list  
*Required*: Yes  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d610c11"></a>

### Ref<a name="w3ab2c21c10d610c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d610c13"></a>

### JSON<a name="aws-resource-elasticache-subnetgroup-example.json"></a>

```
"SubnetGroup" : {
    "Type" : "AWS::ElastiCache::SubnetGroup",
    "Properties" : {
        "Description" : "Cache Subnet Group",
        "SubnetIds" : [ { "Ref" : "Subnet1" }, { "Ref" : "Subnet2" } ]
    }
}
```

### YAML<a name="aws-resource-elasticache-subnetgroup-example.yaml"></a>

```
SubnetGroup: 
  Type: "AWS::ElastiCache::SubnetGroup"
  Properties: 
    Description: "Cache Subnet Group"
    SubnetIds: 
      - Ref: "Subnet1"
      - Ref: "Subnet2"
```