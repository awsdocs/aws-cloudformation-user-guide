# AWS IoT TopicRule DynamoDBAction<a name="aws-properties-iot-topicrule-dynamodbaction"></a>

`DynamoDB` is a property of the `Actions` property that describes an AWS IoT action that writes data to a DynamoDB table\.

The `HashKeyField`, `RangeKeyField`, and `TableName` values must match the values you used when you initially created the table\.

The `HashKeyValue` and `RangeKeyValue` fields use the `${sql-expression}` substitution template syntax\. You can specify any valid expression in a `WHERE` or `SELECT` clause\. This expression can include JSON properties, comparisons, calculations, and functions, for example:

+ The `"HashKeyValue" : "${topic(3)}` field uses the third level of the topic\.

+ The `"RangeKeyValue" : "${timestamp()}` field uses the timestamp\.

## Syntax<a name="w3ab2c21c14e1135c10"></a>

### JSON<a name="aws-properties-iot-topicrule-dynamodbaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-hashkeyfield)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-hashkeytype)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-hashkeyvalue)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-payloadfield)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rangekeyfield)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rangekeytype)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rangekeyvalue)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rolearn)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-tablename)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-dynamodbaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-hashkeyfield): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-hashkeytype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-hashkeyvalue): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-payloadfield): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rangekeyfield): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rangekeytype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rangekeyvalue): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-rolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbaction-tablename): String
```

## Properties<a name="w3ab2c21c14e1135c12"></a>

For more information and valid values, see [DynamoDB Action](http://docs.aws.amazon.com/iot/latest/developerguide/dynamodb-rule.html) in the *AWS IoT Developer Guide*\.

`HashKeyField`  
The name of the hash key\.  
*Required: *Yes  
*Type*: String

`HashKeyType`  
The data type of the hash key \(also called the partition key\)\. Valid values are: `"STRING"` or `"NUMBER"`\.  
*Required: *No  
*Type*: String

`HashKeyValue`  
The value of the hash key\.  
*Required: *Yes  
*Type*: String

`PayloadField`  
The name of the column in the DynamoDB table that contains the result of the query\. You can customize this name\.  
*Required: *No  
*Type*: String

`RangeKeyField`  
The name of the range key\.  
*Required: *Yes  
*Type*: String

`RangeKeyType`  
The data type of the range key \(also called the sort key\)\. Valid values are: `"STRING"` or `"NUMBER"`\.  
*Required: *No  
*Type*: String

`RangeKeyValue`  
The value of the range key\.  
*Required: *Yes  
*Type*: String

`RoleArn`  
The ARN of the IAM role that grants access to the DynamoDB table\.  
*Required: *Yes  
*Type*: String

`TableName`  
The name of the DynamoDB table\.  
*Required: *Yes  
*Type*: String