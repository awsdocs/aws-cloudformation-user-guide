# DynamoDB SSESpecification<a name="aws-properties-dynamodb-table-ssespecification"></a>

The `SSESpecification` property is part of the [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource that specifies the settings to enable server\-side encryption\.

If you do not specify the `SSESpecification` property type, Amazon DynamoDB will create an unencrypted table, the same as if you had specified the `SSESpecification` property type with its `SSEEnabled` property set to `false`\. As a best practice, for consistency only specify the `SSESpecification` property type \(with its `SSEEnabled` property set to `true`\) if you want DynamoDB to create an encrypted table\. 

## Syntax<a name="w3ab2c21c14d631b7"></a>

### JSON<a name="aws-properties-dynamodb-table-ssespecification.json"></a>

```
{
  "[SSEEnabled](#cfn-dynamodb-table-ssespecification-sseenabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-table-ssespecification.yaml"></a>

```
[SSEEnabled](#cfn-dynamodb-table-ssespecification-sseenabled): Boolean
```

## Properties<a name="w3ab2c21c14d631b9"></a>

`SSEEnabled`  <a name="cfn-dynamodb-table-ssespecification-sseenabled"></a>
Whether server\-side encryption is enabled or not\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)