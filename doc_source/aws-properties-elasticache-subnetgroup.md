# AWS::ElastiCache::SubnetGroup<a name="aws-properties-elasticache-subnetgroup"></a>

Creates a cache subnet group\. For more information about cache subnet groups, go to Cache Subnet Groups in the *Amazon ElastiCache User Guide* or go to [CreateCacheSubnetGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheSubnetGroup.html) in the *Amazon ElastiCache API Reference Guide*\. 

## Syntax<a name="aws-properties-elasticache-subnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-subnetgroup-syntax.json"></a>

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

### YAML<a name="aws-properties-elasticache-subnetgroup-syntax.yaml"></a>

```
Type: AWS::ElastiCache::SubnetGroup
Properties: 
  [CacheSubnetGroupName](#cfn-elasticache-subnetgroup-cachesubnetgroupname): String
  [Description](#cfn-elasticache-subnetgroup-description): String
  [SubnetIds](#cfn-elasticache-subnetgroup-subnetids): 
    - String
```

## Properties<a name="aws-properties-elasticache-subnetgroup-properties"></a>

`CacheSubnetGroupName`  <a name="cfn-elasticache-subnetgroup-cachesubnetgroupname"></a>
The name for the cache subnet group\. This value is stored as a lowercase string\.  
Constraints: Must contain no more than 255 alphanumeric characters or hyphens\.  
Example: `mysubnetgroup`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-elasticache-subnetgroup-description"></a>
The description for the cache subnet group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-elasticache-subnetgroup-subnetids"></a>
The EC2 subnet IDs for the cache subnet group\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-elasticache-subnetgroup-return-values"></a>

### Ref<a name="aws-properties-elasticache-subnetgroup-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the resource name\.

 For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-properties-elasticache-subnetgroup--examples"></a>



### <a name="aws-properties-elasticache-subnetgroup--examples--"></a>

#### JSON<a name="aws-properties-elasticache-subnetgroup--examples----json"></a>

```
{
    "SubnetGroup": {
        "Type": "AWS::ElastiCache::SubnetGroup",
        "Properties": {
            "Description": "Cache Subnet Group",
            "SubnetIds": [
                {
                    "Ref": "Subnet1"
                },
                {
                    "Ref": "Subnet2"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-properties-elasticache-subnetgroup--examples----yaml"></a>

```
SubnetGroup:
  Type: 'AWS::ElastiCache::SubnetGroup'
  Properties:
    Description: Cache Subnet Group
    SubnetIds:
      - !Ref Subnet1
      - !Ref Subnet2
```