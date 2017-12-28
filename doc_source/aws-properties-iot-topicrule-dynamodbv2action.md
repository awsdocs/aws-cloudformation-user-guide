# AWS IoT TopicRule DynamoDBv2Action<a name="aws-properties-iot-topicrule-dynamodbv2action"></a>

<a name="aws-properties-iot-topicrule-dynamodbv2action-description"></a>The `DynamoDBv2Action` property type is a property of the `Actions` property that describes an AWS IoT action that writes data to a DynamoDB table\.

<a name="aws-properties-iot-topicrule-dynamodbv2action-inheritance"></a> `DynamoDBv2Action` is a property of the [AWS IoT TopicRule Action](aws-properties-iot-topicrule-action.md) resource\. 

## Syntax<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbv2action-putitem)" : PutItemInput,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbv2action-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbv2action-putitem): 
  PutItemInput
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-dynamodbv2action-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-dynamodbv2action-properties"></a>

For more information, see [DynamoDBv2 Action](http://docs.aws.amazon.com/iot/latest/developerguide/dynamodb-v2-rule.html) in the *AWS IoT Developer Guide\.*\.

`PutItem`  
Specifies the database table to which to write the item for an AWS IoT topic rule\.  
 *Required*: No  
 *Type*:   
 *Update requires*: No interruption 

`RoleArn`  
The IAM role that allows access to the DynamoDB table\. At a minimum, the role must allow the `dynamoDB:PutItem` IAM action\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 