# AWS::ElastiCache::SubnetGroup<a name="aws-resource-elasticache-subnetgroup"></a>

Creates a cache subnet group\. For more information about cache subnet groups, go to Cache Subnet Groups in the *Amazon ElastiCache User Guide* or go to [CreateCacheSubnetGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheSubnetGroup.html) in the *Amazon ElastiCache API Reference Guide*\. 

## Syntax<a name="aws-resource-elasticache-subnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-subnetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::SubnetGroup",
  "Properties" : {
      "[CacheSubnetGroupName](#cfn-elasticache-subnetgroup-cachesubnetgroupname)" : String,
      "[Description](#cfn-elasticache-subnetgroup-description)" : String,
      "[SubnetIds](#cfn-elasticache-subnetgroup-subnetids)" : [ String, ... ],
      "[Tags](#cfn-elasticache-subnetgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-elasticache-subnetgroup-syntax.yaml"></a>

```
Type: AWS::ElastiCache::SubnetGroup
Properties: 
  [CacheSubnetGroupName](#cfn-elasticache-subnetgroup-cachesubnetgroupname): String
  [Description](#cfn-elasticache-subnetgroup-description): String
  [SubnetIds](#cfn-elasticache-subnetgroup-subnetids): 
    - String
  [Tags](#cfn-elasticache-subnetgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-elasticache-subnetgroup-properties"></a>

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

`Tags`  <a name="cfn-elasticache-subnetgroup-tags"></a>
A tag that can be added to an ElastiCache subnet group\. Tags are composed of a Key/Value pair\. You can use tags to categorize and track all your subnet groups\. A tag with a null Value is permitted\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-elasticache-subnetgroup-return-values"></a>

### Ref<a name="aws-resource-elasticache-subnetgroup-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the resource name\.

 For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-elasticache-subnetgroup--examples"></a>



### <a name="aws-resource-elasticache-subnetgroup--examples--"></a>

#### JSON<a name="aws-resource-elasticache-subnetgroup--examples----json"></a>

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

#### YAML<a name="aws-resource-elasticache-subnetgroup--examples----yaml"></a>

```
SubnetGroup:
  Type: 'AWS::ElastiCache::SubnetGroup'
  Properties:
    Description: Cache Subnet Group
    SubnetIds:
      - !Ref Subnet1
      - !Ref Subnet2
```