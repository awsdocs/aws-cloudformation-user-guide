# Amazon DynamoDB Table StreamSpecification<a name="aws-properties-dynamodb-streamspecification"></a>

`StreamSpecification` is a property of the [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource that defines the settings of a DynamoDB table's stream\.

## Syntax<a name="w3ab2c21c14d635b5"></a>

### JSON<a name="aws-properties-dynamodb-streamspecification-syntax.json"></a>

```
{
   "[StreamViewType](#cfn-dynamodb-streamspecification-streamviewtype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-streamspecification-syntax.yaml"></a>

```
[StreamViewType](#cfn-dynamodb-streamspecification-streamviewtype): String
```

## Parameters<a name="w3ab2c21c14d635b7"></a>

`StreamViewType`  <a name="cfn-dynamodb-streamspecification-streamviewtype"></a>
Determines the information that the stream captures when an item in the table is modified\. For valid values, see [StreamSpecification](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_StreamSpecification.html) in the *Amazon DynamoDB API Reference*\.  
*Required*: Yes  
*Type*: String