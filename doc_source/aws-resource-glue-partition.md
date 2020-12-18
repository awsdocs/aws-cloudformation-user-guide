# AWS::Glue::Partition<a name="aws-resource-glue-partition"></a>

The `AWS::Glue::Partition` resource creates an AWS Glue partition, which represents a slice of table data\. For more information, see [CreatePartition Action](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-CreatePartition) and [Partition Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-Partition) in the *AWS Glue Developer Guide*\.

## Syntax<a name="aws-resource-glue-partition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-partition-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Partition",
  "Properties" : {
      "[CatalogId](#cfn-glue-partition-catalogid)" : String,
      "[DatabaseName](#cfn-glue-partition-databasename)" : String,
      "[PartitionInput](#cfn-glue-partition-partitioninput)" : PartitionInput,
      "[TableName](#cfn-glue-partition-tablename)" : String
    }
}
```

### YAML<a name="aws-resource-glue-partition-syntax.yaml"></a>

```
Type: AWS::Glue::Partition
Properties: 
  [CatalogId](#cfn-glue-partition-catalogid): String
  [DatabaseName](#cfn-glue-partition-databasename): String
  [PartitionInput](#cfn-glue-partition-partitioninput): 
    PartitionInput
  [TableName](#cfn-glue-partition-tablename): String
```

## Properties<a name="aws-resource-glue-partition-properties"></a>

`CatalogId`  <a name="cfn-glue-partition-catalogid"></a>
The AWS account ID of the catalog in which the partion is to be created\.  
To specify the account ID, you can use the `Ref` intrinsic function with the `AWS::AccountId` pseudo parameter\. For example: `!Ref AWS::AccountId` 
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseName`  <a name="cfn-glue-partition-databasename"></a>
The name of the catalog database in which to create the partition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PartitionInput`  <a name="cfn-glue-partition-partitioninput"></a>
The structure used to create and update a partition\.  
*Required*: Yes  
*Type*: [PartitionInput](aws-properties-glue-partition-partitioninput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-glue-partition-tablename"></a>
The name of the metadata table in which the partition is to be created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-glue-partition-return-values"></a>

### Ref<a name="aws-resource-glue-partition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the partition name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-glue-partition--seealso"></a>
+  [CreatePartition Action](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-CreatePartition) in the *AWS Glue Developer Guide* 
+  [Partition Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-partitions.html#aws-glue-api-catalog-partitions-Partition) in the *AWS Glue Developer Guide* 

