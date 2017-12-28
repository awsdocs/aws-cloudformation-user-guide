# Amazon DynamoDB Table StreamSpecification<a name="aws-properties-dynamodb-streamspecification"></a>

`StreamSpecification` is a property of the  resource that defines the settings of a DynamoDB table's stream\.

## Syntax<a name="w3ab2c21c14d545b5"></a>

### JSON<a name="aws-properties-dynamodb-streamspecification-syntax.json"></a>

```
{
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-streamspecification-streamviewtype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-streamspecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-streamspecification-streamviewtype): String
```

## Parameters<a name="w3ab2c21c14d545b7"></a>

`StreamViewType`  
Determines the information that the stream captures when an item in the table is modified\. For valid values, see [StreamSpecification](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_StreamSpecification.html) in the *Amazon DynamoDB API Reference*\.  
*Required: *Yes  
*Type*: String