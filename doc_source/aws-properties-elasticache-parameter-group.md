# AWS::ElastiCache::ParameterGroup<a name="aws-properties-elasticache-parameter-group"></a>

The `AWS::ElastiCache::ParameterGroup` type creates a new cache parameter group\. Cache parameter groups control the parameters for a cache cluster\. 

**Note**  
Updates are not supported\.

## Syntax<a name="aws-properties-elasticache-parameter-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-parameter-group-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::ParameterGroup",
  "Properties" : {
      "[CacheParameterGroupFamily](#cfn-elasticache-parametergroup-cacheparametergroupfamily)" : String,
      "[Description](#cfn-elasticache-parametergroup-description)" : String,
      "[Properties](#cfn-elasticache-parametergroup-properties)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-properties-elasticache-parameter-group-syntax.yaml"></a>

```
Type: AWS::ElastiCache::ParameterGroup
Properties: 
  [CacheParameterGroupFamily](#cfn-elasticache-parametergroup-cacheparametergroupfamily): String
  [Description](#cfn-elasticache-parametergroup-description): String
  [Properties](#cfn-elasticache-parametergroup-properties): 
    Key : Value
```

## Properties<a name="aws-properties-elasticache-parameter-group-properties"></a>

`CacheParameterGroupFamily`  <a name="cfn-elasticache-parametergroup-cacheparametergroupfamily"></a>
The name of the cache parameter group family that this cache parameter group is compatible with\.  
Valid values are: `memcached1.4` \| `memcached1.5` \| `memcached1.6` \| `redis2.6` \| `redis2.8` \| `redis3.2` \| `redis4.0` \| `redis5.0` \| `redis6.x`   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-elasticache-parametergroup-description"></a>
The description for this cache parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Properties`  <a name="cfn-elasticache-parametergroup-properties"></a>
A comma\-delimited list of parameter name/value pairs\. For more information, see [ModifyCacheParameterGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_ModifyCacheParameterGroup.html) in the *Amazon ElastiCache API Reference Guide*\.   
For example:   

```
"Properties" : {
   "cas_disabled" : "1",
   "chunk_size_growth_factor" : "1.02"
}
```
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-elasticache-parameter-group-return-values"></a>

### Ref<a name="aws-properties-elasticache-parameter-group-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-elasticache-parameter-group--examples"></a>



### <a name="aws-properties-elasticache-parameter-group--examples--"></a>

#### JSON<a name="aws-properties-elasticache-parameter-group--examples----json"></a>

```
{
    "MyParameterGroup": {
        "Type": "AWS::ElastiCache::ParameterGroup",
        "Properties": {
            "Description": "MyNewParameterGroup",
            "CacheParameterGroupFamily": "memcached1.4",
            "Properties": {
                "cas_disabled": "1",
                "chunk_size_growth_factor": "1.02"
            }
        }
    }
}
```

#### YAML<a name="aws-properties-elasticache-parameter-group--examples----yaml"></a>

```
MyParameterGroup:
  Type: 'AWS::ElastiCache::ParameterGroup'
  Properties:
    Description: MyNewParameterGroup
    CacheParameterGroupFamily: memcached1.4
    Properties:
      cas_disabled: '1'
      chunk_size_growth_factor: '1.02'
```

## See also<a name="aws-properties-elasticache-parameter-group--seealso"></a>
+ [CreateCacheParameterGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheParameterGroup.html) in the * Amazon ElastiCache API Reference Guide* 
+ [ModifyCacheParameterGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_ModifyCacheParameterGroup.html) in the * Amazon ElastiCache API Reference Guide* 
+ [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) 