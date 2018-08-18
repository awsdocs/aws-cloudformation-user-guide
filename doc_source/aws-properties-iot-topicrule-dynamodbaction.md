# AWS IoT TopicRule DynamoDBAction<a name="aws-properties-iot-topicrule-dynamodbaction"></a>

`DynamoDB` is a property of the `Actions` property that describes an AWS IoT action that writes data to a DynamoDB table\.

The `HashKeyField`, `RangeKeyField`, and `TableName` values must match the values you used when you initially created the table\.

The `HashKeyValue` and `RangeKeyValue` fields use the `${sql-expression}` substitution template syntax\. You can specify any valid expression in a `WHERE` or `SELECT` clause\. This expression can include JSON properties, comparisons, calculations, and functions, for example:
+ The `"HashKeyValue" : "${topic(3)}` field uses the third level of the topic\.
+ The `"RangeKeyValue" : "${timestamp()}` field uses the timestamp\.

## Syntax<a name="w3ab2c21c14e1332c10"></a>

### JSON<a name="aws-properties-iot-topicrule-dynamodbaction-syntax.json"></a>

```
{
  "[HashKeyField](#cfn-iot-topicrule-dynamodbaction-hashkeyfield)": String,
  "[HashKeyType](#cfn-iot-topicrule-dynamodbaction-hashkeytype)": String,
  "[HashKeyValue](#cfn-iot-topicrule-dynamodbaction-hashkeyvalue)": String,
  "[PayloadField](#cfn-iot-topicrule-dynamodbaction-payloadfield)": String,
  "[RangeKeyField](#cfn-iot-topicrule-dynamodbaction-rangekeyfield)": String,
  "[RangeKeyType](#cfn-iot-topicrule-dynamodbaction-rangekeytype)": String,
  "[RangeKeyValue](#cfn-iot-topicrule-dynamodbaction-rangekeyvalue)": String,
  "[RoleArn](#cfn-iot-topicrule-dynamodbaction-rolearn)": String,
  "[TableName](#cfn-iot-topicrule-dynamodbaction-tablename)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-dynamodbaction-syntax.yaml"></a>

```
[HashKeyField](#cfn-iot-topicrule-dynamodbaction-hashkeyfield): String
[HashKeyType](#cfn-iot-topicrule-dynamodbaction-hashkeytype): String
[HashKeyValue](#cfn-iot-topicrule-dynamodbaction-hashkeyvalue): String
[PayloadField](#cfn-iot-topicrule-dynamodbaction-payloadfield): String
[RangeKeyField](#cfn-iot-topicrule-dynamodbaction-rangekeyfield): String
[RangeKeyType](#cfn-iot-topicrule-dynamodbaction-rangekeytype): String
[RangeKeyValue](#cfn-iot-topicrule-dynamodbaction-rangekeyvalue): String
[RoleArn](#cfn-iot-topicrule-dynamodbaction-rolearn): String
[TableName](#cfn-iot-topicrule-dynamodbaction-tablename): String
```

## Properties<a name="w3ab2c21c14e1332c12"></a>

For more information and valid values, see [DynamoDB Action](http://docs.aws.amazon.com/iot/latest/developerguide/dynamodb-rule.html) in the *AWS IoT Developer Guide*\.

`HashKeyField`  <a name="cfn-iot-topicrule-dynamodbaction-hashkeyfield"></a>
The name of the hash key\.  
*Required*: Yes  
*Type*: String

`HashKeyType`  <a name="cfn-iot-topicrule-dynamodbaction-hashkeytype"></a>
The data type of the hash key \(also called the partition key\)\. Valid values are: `"STRING"` or `"NUMBER"`\.  
*Required*: No  
*Type*: String

`HashKeyValue`  <a name="cfn-iot-topicrule-dynamodbaction-hashkeyvalue"></a>
The value of the hash key\.  
*Required*: Yes  
*Type*: String

`PayloadField`  <a name="cfn-iot-topicrule-dynamodbaction-payloadfield"></a>
The name of the column in the DynamoDB table that contains the result of the query\. You can customize this name\.  
*Required*: No  
*Type*: String

`RangeKeyField`  <a name="cfn-iot-topicrule-dynamodbaction-rangekeyfield"></a>
The name of the range key\.  
*Required*: No  
*Type*: String

`RangeKeyType`  <a name="cfn-iot-topicrule-dynamodbaction-rangekeytype"></a>
The data type of the range key \(also called the sort key\)\. Valid values are: `"STRING"` or `"NUMBER"`\.  
*Required*: No  
*Type*: String

`RangeKeyValue`  <a name="cfn-iot-topicrule-dynamodbaction-rangekeyvalue"></a>
The value of the range key\.  
*Required*: No  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-dynamodbaction-rolearn"></a>
The ARN of the IAM role that grants access to the DynamoDB table\.  
*Required*: Yes  
*Type*: String

`TableName`  <a name="cfn-iot-topicrule-dynamodbaction-tablename"></a>
The name of the DynamoDB table\.  
*Required*: Yes  
*Type*: String