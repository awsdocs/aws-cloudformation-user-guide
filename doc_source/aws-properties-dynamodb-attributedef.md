# Amazon DynamoDB Table AttributeDefinition<a name="aws-properties-dynamodb-attributedef"></a>

The `AttributeDefinition` property type represents an attribute for describing the key schema for a DynamoDB table and indexes\.

**Note**  
AWS CloudFormation uses these attributes to provision the keys for the table\. They don't represent the full schema of the table\.

The `AttributeDefinition` property of the [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource contains a list of `AttributeDefinition` property types\.

## Syntax<a name="w3ab2c21c14d599b9"></a>

### JSON<a name="aws-properties-dynamodb-attributedef-syntax.json"></a>

```
{
  "[AttributeName](#cfn-dynamodb-attributedef-attributename)" : String,
  "[AttributeType](#cfn-dynamodb-attributedef-attributename-attributetype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-attributedef-syntax.yaml"></a>

```
[AttributeName](#cfn-dynamodb-attributedef-attributename): String
[AttributeType](#cfn-dynamodb-attributedef-attributename-attributetype): String
```

## Properties<a name="w3ab2c21c14d599c11"></a>

`AttributeName`  <a name="cfn-dynamodb-attributedef-attributename"></a>
The name of an attribute\. Attribute names can be 1 – 255 characters long and have no character restrictions\.  
*Required*: Yes  
*Type*: String

`AttributeType`  <a name="cfn-dynamodb-attributedef-attributename-attributetype"></a>
The data type for the attribute\. You can specify `S` for string data, `N` for numeric data, or `B` for binary data\.  
*Required*: Yes  
*Type*: String