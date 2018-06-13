# AWS::ElastiCache::ParameterGroup<a name="aws-properties-elasticache-parameter-group"></a>

The AWS::ElastiCache::ParameterGroup type creates a new cache parameter group\. Cache parameter groups control the parameters for a cache cluster\.

**Topics**
+ [Syntax](#aws-resource-elasticache-parametergroup-syntax)
+ [Properties](#aws-properties-elasticache-parameter-group-prop)
+ [Return Values](#w3ab2c21c10d589c11)
+ [Example](#w3ab2c21c10d589c13)
+ [See Also](#w3ab2c21c10d589c15)

## Syntax<a name="aws-resource-elasticache-parametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-parametergroup-syntax.json"></a>

```
{
   "Type": "AWS::ElastiCache::ParameterGroup",
   "Properties": {
      "CacheParameterGroupFamily" : String,
      "Description" : String,
      "Properties" : { String:String, ... }
   }
}
```

### YAML<a name="aws-resource-elasticache-parametergroup-syntax.yaml"></a>

```
Type: "AWS::ElastiCache::ParameterGroup"
Properties: 
  CacheParameterGroupFamily: String
  Description: String
  Properties:
    String: String
```

## Properties<a name="aws-properties-elasticache-parameter-group-prop"></a>

`CacheParameterGroupFamily`  <a name="cfn-elasticache-parametergroup-cacheparametergroupfamily"></a>
The name of the cache parameter group family that the cache parameter group can be used with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Description`  <a name="cfn-elasticache-parametergroup-description"></a>
The description for the Cache Parameter Group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Properties`  <a name="cfn-elasticache-parametergroup-properties"></a>
A comma\-delimited list of parameter name/value pairs\. For more information, go to [ModifyCacheParameterGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_ModifyCacheParameterGroup.html) in the *Amazon ElastiCache API Reference Guide*\.  
*Example*:  

```
"Properties" : {
   "cas_disabled" : "1",
   "chunk_size_growth_factor" : "1.02"
}
```
*Required*: No  
*Type*: Mapping of key\-value pairs  
*Update requires*: Updates are not supported\.

## Return Values<a name="w3ab2c21c10d589c11"></a>

### Ref<a name="aws-properties-elasticache-parameter-group-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d589c13"></a>

### JSON<a name="aws-resource-elasticache-parametergroup-example.json"></a>

```
"MyParameterGroup": {
   "Type": "AWS::ElastiCache::ParameterGroup",
   "Properties": {
      "Description": "MyNewParameterGroup",
      "CacheParameterGroupFamily": "memcached1.4",
      "Properties" : {
         "cas_disabled" : "1",
         "chunk_size_growth_factor" : "1.02"
      }
   }
}
```

### YAML<a name="aws-resource-elasticache-parametergroup-example.yaml"></a>

```
MyParameterGroup: 
  Type: "AWS::ElastiCache::ParameterGroup"
  Properties: 
    Description: "MyNewParameterGroup"
    CacheParameterGroupFamily: "memcached1.4"
    Properties: 
      cas_disabled: "1"
      chunk_size_growth_factor: "1.02"
```

## See Also<a name="w3ab2c21c10d589c15"></a>
+ [CreateCacheParameterGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheParameterGroup.html) in the *Amazon ElastiCache API Reference Guide*
+ [ModifyCacheParameterGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_ModifyCacheParameterGroup.html) in the *Amazon ElastiCache API Reference Guide*
+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)