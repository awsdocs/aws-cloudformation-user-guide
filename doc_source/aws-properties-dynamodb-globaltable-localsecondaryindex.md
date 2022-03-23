# AWS::DynamoDB::GlobalTable LocalSecondaryIndex<a name="aws-properties-dynamodb-globaltable-localsecondaryindex"></a>

Represents the properties of a local secondary index\. A local secondary index can only be created when its parent table is created\.

## Syntax<a name="aws-properties-dynamodb-globaltable-localsecondaryindex-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-localsecondaryindex-syntax.json"></a>

```
{
  "[IndexName](#cfn-dynamodb-globaltable-localsecondaryindex-indexname)" : String,
  "[KeySchema](#cfn-dynamodb-globaltable-localsecondaryindex-keyschema)" : [ KeySchema, ... ],
  "[Projection](#cfn-dynamodb-globaltable-localsecondaryindex-projection)" : Projection
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-localsecondaryindex-syntax.yaml"></a>

```
  [IndexName](#cfn-dynamodb-globaltable-localsecondaryindex-indexname): String
  [KeySchema](#cfn-dynamodb-globaltable-localsecondaryindex-keyschema): 
    - KeySchema
  [Projection](#cfn-dynamodb-globaltable-localsecondaryindex-projection): 
    Projection
```

## Properties<a name="aws-properties-dynamodb-globaltable-localsecondaryindex-properties"></a>

`IndexName`  <a name="cfn-dynamodb-globaltable-localsecondaryindex-indexname"></a>
The name of the local secondary index\. The name must be unique among all other indexes on this table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: Updates are not supported\.

`KeySchema`  <a name="cfn-dynamodb-globaltable-localsecondaryindex-keyschema"></a>
The complete key schema for the local secondary index, consisting of one or more pairs of attribute names and key types:  
+  `HASH` \- partition key
+  `RANGE` \- sort key
The partition key of an item is also known as its *hash attribute*\. The term "hash attribute" derives from DynamoDB's usage of an internal hash function to evenly distribute data items across partitions, based on their partition key values\.  
The sort key of an item is also known as its *range attribute*\. The term "range attribute" derives from the way DynamoDB stores items with the same partition key physically close together, in sorted order by the sort key value\.
*Required*: Yes  
*Type*: [List](aws-properties-dynamodb-globaltable-keyschema.md) of [KeySchema](aws-properties-dynamodb-globaltable-keyschema.md)  
*Maximum*: `2`  
*Update requires*: Updates are not supported\.

`Projection`  <a name="cfn-dynamodb-globaltable-localsecondaryindex-projection"></a>
Represents attributes that are copied \(projected\) from the table into the local secondary index\. These are in addition to the primary key attributes and index key attributes, which are automatically projected\.   
*Required*: Yes  
*Type*: [Projection](aws-properties-dynamodb-globaltable-projection.md)  
*Update requires*: Updates are not supported\.