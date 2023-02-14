# AWS::DynamoDB::GlobalTable GlobalSecondaryIndex<a name="aws-properties-dynamodb-globaltable-globalsecondaryindex"></a>

Allows you to specify a global secondary index for the global table\. The index will be defined on all replicas\.

## Syntax<a name="aws-properties-dynamodb-globaltable-globalsecondaryindex-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-globalsecondaryindex-syntax.json"></a>

```
{
  "[IndexName](#cfn-dynamodb-globaltable-globalsecondaryindex-indexname)" : String,
  "[KeySchema](#cfn-dynamodb-globaltable-globalsecondaryindex-keyschema)" : [ KeySchema, ... ],
  "[Projection](#cfn-dynamodb-globaltable-globalsecondaryindex-projection)" : Projection,
  "[WriteProvisionedThroughputSettings](#cfn-dynamodb-globaltable-globalsecondaryindex-writeprovisionedthroughputsettings)" : WriteProvisionedThroughputSettings
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-globalsecondaryindex-syntax.yaml"></a>

```
  [IndexName](#cfn-dynamodb-globaltable-globalsecondaryindex-indexname): String
  [KeySchema](#cfn-dynamodb-globaltable-globalsecondaryindex-keyschema): 
    - KeySchema
  [Projection](#cfn-dynamodb-globaltable-globalsecondaryindex-projection): 
    Projection
  [WriteProvisionedThroughputSettings](#cfn-dynamodb-globaltable-globalsecondaryindex-writeprovisionedthroughputsettings): 
    WriteProvisionedThroughputSettings
```

## Properties<a name="aws-properties-dynamodb-globaltable-globalsecondaryindex-properties"></a>

`IndexName`  <a name="cfn-dynamodb-globaltable-globalsecondaryindex-indexname"></a>
The name of the global secondary index\. The name must be unique among all other indexes on this table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: Updates are not supported\.

`KeySchema`  <a name="cfn-dynamodb-globaltable-globalsecondaryindex-keyschema"></a>
The complete key schema for a global secondary index, which consists of one or more pairs of attribute names and key types:  
+  `HASH` \- partition key
+  `RANGE` \- sort key
The partition key of an item is also known as its *hash attribute*\. The term "hash attribute" derives from DynamoDB's usage of an internal hash function to evenly distribute data items across partitions, based on their partition key values\.  
The sort key of an item is also known as its *range attribute*\. The term "range attribute" derives from the way DynamoDB stores items with the same partition key physically close together, in sorted order by the sort key value\.
*Required*: Yes  
*Type*: [List](aws-properties-dynamodb-globaltable-keyschema.md) of [KeySchema](aws-properties-dynamodb-globaltable-keyschema.md)  
*Maximum*: `2`  
*Update requires*: Updates are not supported\.

`Projection`  <a name="cfn-dynamodb-globaltable-globalsecondaryindex-projection"></a>
Represents attributes that are copied \(projected\) from the table into the global secondary index\. These are in addition to the primary key attributes and index key attributes, which are automatically projected\.  
*Required*: Yes  
*Type*: [Projection](aws-properties-dynamodb-globaltable-projection.md)  
*Update requires*: Updates are not supported\.

`WriteProvisionedThroughputSettings`  <a name="cfn-dynamodb-globaltable-globalsecondaryindex-writeprovisionedthroughputsettings"></a>
Defines write capacity settings for the global secondary index\. You must specify a value for this property if the table's `BillingMode` is `PROVISIONED`\. All replicas will have the same write capacity settings for this global secondary index\.  
*Required*: No  
*Type*: [WriteProvisionedThroughputSettings](aws-properties-dynamodb-globaltable-writeprovisionedthroughputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)