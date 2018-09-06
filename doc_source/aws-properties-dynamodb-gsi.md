# Amazon DynamoDB Table GlobalSecondaryIndex<a name="aws-properties-dynamodb-gsi"></a>

Describes global secondary indexes for the [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource\.

## Syntax<a name="w3ab2c21c14d604b5"></a>

### JSON<a name="aws-properties-dynamodb-gsi-syntax.json"></a>

```
{
  "[IndexName](#cfn-dynamodb-gsi-indexname)" : String,
  "[KeySchema](#cfn-dynamodb-gsi-keyschema)" : [ KeySchema, ... ],
  "[Projection](#cfn-dynamodb-gsi-projection)" : { Projection },
  "[ProvisionedThroughput](#cfn-dynamodb-gsi-provisionthroughput)" : { ProvisionedThroughput }
}
```

### YAML<a name="aws-properties-dynamodb-gsi-syntax.yaml"></a>

```
[IndexName](#cfn-dynamodb-gsi-indexname): String
[KeySchema](#cfn-dynamodb-gsi-keyschema):
  - KeySchema
[Projection](#cfn-dynamodb-gsi-projection):
  Projection
[ProvisionedThroughput](#cfn-dynamodb-gsi-provisionthroughput):
  ProvisionedThroughput
```

## Properties<a name="w3ab2c21c14d604b7"></a>

`IndexName`  <a name="cfn-dynamodb-gsi-indexname"></a>
The name of the global secondary index\. The index name can be 3 – 255 characters long and must satisfy the regular expression pattern `[a-zA-Z0-9_.-]+`\.  
*Required*: Yes  
*Type*: String

`KeySchema`  <a name="cfn-dynamodb-gsi-keyschema"></a>
The complete index key schema for the global secondary index, which consists of one or more pairs of attribute names and key types\.  
*Required*: Yes  
*Type*: List of [DynamoDB Table KeySchema](aws-properties-dynamodb-keyschema.md)

`Projection`  <a name="cfn-dynamodb-gsi-projection"></a>
Attributes that are copied \(projected\) from the source table into the index\. These attributes are in addition to the primary key attributes and index key attributes, which are automatically projected\.  
*Required*: Yes  
*Type*: [DynamoDB Table Projection](aws-properties-dynamodb-projectionobject.md)

`ProvisionedThroughput`  <a name="cfn-dynamodb-gsi-provisionthroughput"></a>
The provisioned throughput settings for the index\.  
*Required*: Yes  
*Type*: [DynamoDB Table ProvisionedThroughput](aws-properties-dynamodb-provisionedthroughput.md)