# AWS::DynamoDB::Table LocalSecondaryIndex<a name="aws-properties-dynamodb-lsi"></a>

Represents the properties of a local secondary index\.

## Syntax<a name="aws-properties-dynamodb-lsi-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-lsi-syntax.json"></a>

```
{
  "[IndexName](#cfn-dynamodb-lsi-indexname)" : String,
  "[KeySchema](#cfn-dynamodb-lsi-keyschema)" : [ KeySchema, ... ],
  "[Projection](#cfn-dynamodb-lsi-projection)" : Projection
}
```

### YAML<a name="aws-properties-dynamodb-lsi-syntax.yaml"></a>

```
  [IndexName](#cfn-dynamodb-lsi-indexname): String
  [KeySchema](#cfn-dynamodb-lsi-keyschema): 
    - KeySchema
  [Projection](#cfn-dynamodb-lsi-projection): 
    Projection
```

## Properties<a name="aws-properties-dynamodb-lsi-properties"></a>

`IndexName`  <a name="cfn-dynamodb-lsi-indexname"></a>
The name of the local secondary index\. The name must be unique among all other indexes on this table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeySchema`  <a name="cfn-dynamodb-lsi-keyschema"></a>
The complete key schema for the local secondary index, consisting of one or more pairs of attribute names and key types:  
+  `HASH` \- partition key
+  `RANGE` \- sort key
The partition key of an item is also known as its *hash attribute*\. The term "hash attribute" derives from DynamoDB's usage of an internal hash function to evenly distribute data items across partitions, based on their partition key values\.  
The sort key of an item is also known as its *range attribute*\. The term "range attribute" derives from the way DynamoDB stores items with the same partition key physically close together, in sorted order by the sort key value\.
*Required*: Yes  
*Type*: [List](aws-properties-dynamodb-keyschema.md) of [KeySchema](aws-properties-dynamodb-keyschema.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Projection`  <a name="cfn-dynamodb-lsi-projection"></a>
Represents attributes that are copied \(projected\) from the table into the local secondary index\. These are in addition to the primary key attributes and index key attributes, which are automatically projected\.   
*Required*: Yes  
*Type*: [Projection](aws-properties-dynamodb-projectionobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-dynamodb-lsi--seealso"></a>

For an example of a declared local secondary index, see [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)\. 