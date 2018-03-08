# AWS IoT TopicRule PutItemInput<a name="aws-properties-iot-topicrule-putiteminput"></a>

<a name="aws-properties-iot-topicrule-putiteminput-description"></a>The `PutItemInput` property type specifies the database table for an AWS IoT topic rule\.

<a name="aws-properties-iot-topicrule-putiteminput-inheritance"></a> `PutItemInput` is a property of the [AWS IoT TopicRule DynamoDBv2Action](aws-properties-iot-topicrule-dynamodbv2action.md) property type\. 

## Syntax<a name="aws-properties-iot-topicrule-putiteminput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-putiteminput-syntax.json"></a>

```
{
  "[TableName](#cfn-iot-topicrule-putiteminput-tablename)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-putiteminput-syntax.yaml"></a>

```
[TableName](#cfn-iot-topicrule-putiteminput-tablename): String
```

## Properties<a name="aws-properties-iot-topicrule-putiteminput-properties"></a>

`TableName`  <a name="cfn-iot-topicrule-putiteminput-tablename"></a>
The name of the DynamoDB table\.  
The MQTT message payload must contain a root\-level key that matches the table's primary partition key and a root\-level key that matches the table's primary sort key, if one is defined\. For more information, see [DynamoDBv2 Action](http://docs.aws.amazon.com/iot/latest/developerguide/dynamodb-v2-rule.html) in the *AWS IoT Developer Guide\.*\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 