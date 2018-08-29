# Amazon DynamoDB Table KeySchema<a name="aws-properties-dynamodb-keyschema"></a>

Describes a primary key for the [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource or a key schema for an index\. Each element is composed of an `AttributeName` and `KeyType`\.

For the primary key of an Amazon DynamoDB table that consists of only a hash attribute, specify one element with a `KeyType` of `HASH`\. For the primary key of an Amazon DynamoDB table that consists of a hash and range attributes, specify two elements: one with a `KeyType` of `HASH` and one with a `KeyType` of `RANGE`\.

For a complete discussion of DynamoDB primary keys, see [Primary Key](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DataModel.html#DataModelPrimaryKey) in the *Amazon DynamoDB Developer Guide*\.

## Syntax<a name="w3ab2c21c14d609b9"></a>

### JSON<a name="aws-properties-dynamodb-keyschema-syntax.json"></a>

```
{
  "[AttributeName](#cfn-dynamodb-keyschema-attributename)" : String,
  "[KeyType](#cfn-dynamodb-keyschema-keytype)" : "HASH or RANGE"
}
```

### YAML<a name="aws-properties-dynamodb-keyschema-syntax.yaml"></a>

```
[AttributeName](#cfn-dynamodb-keyschema-attributename): String
[KeyType](#cfn-dynamodb-keyschema-keytype): HASH or RANGE
```

## Properties<a name="w3ab2c21c14d609c11"></a>

`AttributeName`  <a name="cfn-dynamodb-keyschema-attributename"></a>
The attribute name that is used as the primary key for this table\. Primary key element names can be 1 – 255 characters long and have no character restrictions\.  
*Required*: Yes  
*Type*: String

`KeyType`  <a name="cfn-dynamodb-keyschema-keytype"></a>
Represents the attribute data, consisting of the data type and the attribute value itself\. You can specify `HASH` or `RANGE`\.  
*Required*: Yes  
*Type*: String

## Examples<a name="w3ab2c21c14d609c13"></a>

For an example of a declared key schema, see [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)\.