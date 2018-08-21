# AWS::Glue::Partition<a name="aws-resource-glue-partition"></a>

The `AWS::Glue::Partition` resource creates an AWS Glue partition, which represents a slice of table data\. For more information, see [CreatePartition Action](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-CreatePartition) and [Partition Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-Partition) in the *AWS Glue Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-glue-partition-syntax)
+ [Properties](#aws-resource-glue-partition-properties)
+ [See Also](#aws-resource-glue-partition-seealso)

## Syntax<a name="aws-resource-glue-partition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-partition-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Partition",
  "Properties" : {
    "[TableName](#cfn-glue-partition-tablename)" : String,
    "[DatabaseName](#cfn-glue-partition-databasename)" : String,
    "[CatalogId](#cfn-glue-partition-catalogid)" : String,
    "[PartitionInput](#cfn-glue-partition-partitioninput)" : [*PartitionInput*](aws-properties-glue-partition-partitioninput.md)
  }
}
```

### YAML<a name="aws-resource-glue-partition-syntax.yaml"></a>

```
Type: "AWS::Glue::Partition"
Properties:
  [TableName](#cfn-glue-partition-tablename): String
  [DatabaseName](#cfn-glue-partition-databasename): String
  [CatalogId](#cfn-glue-partition-catalogid): String
  [PartitionInput](#cfn-glue-partition-partitioninput): 
    [*PartitionInput*](aws-properties-glue-partition-partitioninput.md)
```

## Properties<a name="aws-resource-glue-partition-properties"></a>

`TableName`  <a name="cfn-glue-partition-tablename"></a>
The name of the metadata table to create the partition in\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DatabaseName`  <a name="cfn-glue-partition-databasename"></a>
The name of the catalog database to create the partition in\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CatalogId`  <a name="cfn-glue-partition-catalogid"></a>
The ID of the data catalog to create the catalog object in\. Currently, this should be the AWS account ID\.  
To specify the account ID, you can use the `Ref` intrinsic function with the `AWS::AccountId` pseudo parameter—for example `!Ref AWS::AccountId`\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PartitionInput`  <a name="cfn-glue-partition-partitioninput"></a>
The metadata of the partition\.  
 *Required*: Yes  
 *Type*: [AWS Glue Partition PartitionInput](aws-properties-glue-partition-partitioninput.md)  
 *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) 

## See Also<a name="aws-resource-glue-partition-seealso"></a>
+ [CreatePartition Action](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-CreatePartition) in the *AWS Glue Developer Guide*
+ [Partition Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-Partition) in the *AWS Glue Developer Guide*