# AWS Glue Partition PartitionInput<a name="aws-properties-glue-partition-partitioninput"></a>

<a name="aws-properties-glue-partition-partitioninput-description"></a>The `PartitionInput` property type specifies the metadata that's used to create or update an AWS Glue partition\.

<a name="aws-properties-glue-partition-partitioninput-inheritance"></a> `PartitionInput` is a property of the [AWS::Glue::Partition](aws-resource-glue-partition.md) resource\.

## Syntax<a name="aws-properties-glue-partition-partitioninput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-partitioninput-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-partitioninput-parameters)" : JSON object,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-partitioninput-storagedescriptor)" : StorageDescriptor,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-partitioninput-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-glue-partition-partitioninput-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-partitioninput-parameters): 
  JSON object
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-partitioninput-storagedescriptor): 
  StorageDescriptor
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-partitioninput-values): 
  - String
```

## Properties<a name="aws-properties-glue-partition-partitioninput-properties"></a>

`Parameters`  
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the parameters for the partition\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`StorageDescriptor`  
Information about the physical storage of the partition\.  
 *Required*: No  
 *Type*: [AWS Glue Partition StorageDescriptor](aws-properties-glue-partition-storagedescriptor.md)  
 *Update requires*: No interruption 

`Values`  
A list of UTF\-8 strings that specify the values of the partition\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: Replacement 

## See Also<a name="aws-properties-glue-partition-partitioninput-seealso"></a>

+ [PartitionInput](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-PartitionInput) in the *AWS Glue Developer Guide*