# AWS::DynamoDB::Table KeySchema<a name="aws-properties-dynamodb-keyschema"></a>

Represents *a single element* of a key schema\. A key schema specifies the attributes that make up the primary key of a table, or the key attributes of an index\.

A `KeySchemaElement` represents exactly one attribute of the primary key\. For example, a simple primary key would be represented by one `KeySchemaElement` \(for the partition key\)\. A composite primary key would require one `KeySchemaElement` for the partition key, and another `KeySchemaElement` for the sort key\.

A `KeySchemaElement` must be a scalar, top\-level attribute \(not a nested attribute\)\. The data type must be one of String, Number, or Binary\. The attribute cannot be nested within a List or a Map\.

## Syntax<a name="aws-properties-dynamodb-keyschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-keyschema-syntax.json"></a>

```
{
  "[AttributeName](#aws-properties-dynamodb-keyschema-attributename)" : String,
  "[KeyType](#aws-properties-dynamodb-keyschema-keytype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-keyschema-syntax.yaml"></a>

```
  [AttributeName](#aws-properties-dynamodb-keyschema-attributename): String
  [KeyType](#aws-properties-dynamodb-keyschema-keytype): String
```

## Properties<a name="aws-properties-dynamodb-keyschema-properties"></a>

`AttributeName`  <a name="aws-properties-dynamodb-keyschema-attributename"></a>
The name of a key attribute\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyType`  <a name="aws-properties-dynamodb-keyschema-keytype"></a>
The role that this key attribute will assume:  
+  `HASH` \- partition key
+  `RANGE` \- sort key
The partition key of an item is also known as its *hash attribute*\. The term "hash attribute" derives from DynamoDB's usage of an internal hash function to evenly distribute data items across partitions, based on their partition key values\.  
The sort key of an item is also known as its *range attribute*\. The term "range attribute" derives from the way DynamoDB stores items with the same partition key physically close together, in sorted order by the sort key value\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-dynamodb-keyschema--seealso"></a>

For an example of a declared key schema, see [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)\. 