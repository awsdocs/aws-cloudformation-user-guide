# Amazon EMR Cluster KeyValue<a name="aws-properties-elasticmapreduce-cluster-keyvalue"></a>

<a name="aws-properties-elasticmapreduce-cluster-keyvalue-description"></a>The `KeyValue` property type specifies a key value pair\.

<a name="aws-properties-elasticmapreduce-cluster-keyvalue-inheritance"></a> `KeyValue` is a property of the [Amazon EMR Cluster HadoopJarStepConfig](aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig.md) property type\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-keyvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-keyvalue-syntax.json"></a>

```
{
  "[Key](#cfn-elasticmapreduce-cluster-keyvalue-key)" : String,
  "[Value](#cfn-elasticmapreduce-cluster-keyvalue-value)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-keyvalue-syntax.yaml"></a>

```
[Key](#cfn-elasticmapreduce-cluster-keyvalue-key): String
[Value](#cfn-elasticmapreduce-cluster-keyvalue-value): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-keyvalue-properties"></a>

`Key`  <a name="cfn-elasticmapreduce-cluster-keyvalue-key"></a>
The unique identifier of a key value pair\.  
Length Constraints: Minimum length of 0\. Maximum length of 10280\.  
Pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-elasticmapreduce-cluster-keyvalue-value"></a>
The value part of the identified key\.  
Length Constraints: Minimum length of 0\. Maximum length of 10280\.  
Pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-elasticmapreduce-cluster-keyvalue-seealso"></a>
+ [KeyValue](https://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_KeyValue.html) in the *Amazon EMR API Reference*