# AWS IoT TopicRule DynamoDBv2Action<a name="aws-properties-iot-topicrule-dynamodbv2action"></a>

<a name="aws-properties-iot-topicrule-dynamodbv2action-description"></a>The `DynamoDBv2Action` property type is a property of the `Actions` property that describes an AWS IoT action that writes data to a DynamoDB table\.

<a name="aws-properties-iot-topicrule-dynamodbv2action-inheritance"></a> `DynamoDBv2Action` is a property of the [AWS IoT TopicRule Action](aws-properties-iot-topicrule-action.md) resource\. 

## Syntax<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax.json"></a>

```
{
  "[PutItem](#cfn-iot-topicrule-dynamodbv2action-putitem)" : [*PutItemInput*](aws-properties-iot-topicrule-putiteminput.md),
  "[RoleArn](#cfn-iot-topicrule-dynamodbv2action-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax.yaml"></a>

```
[PutItem](#cfn-iot-topicrule-dynamodbv2action-putitem): 
  [*PutItemInput*](aws-properties-iot-topicrule-putiteminput.md)
[RoleArn](#cfn-iot-topicrule-dynamodbv2action-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-dynamodbv2action-properties"></a>

For more information, see [DynamoDBv2 Action](http://docs.aws.amazon.com/iot/latest/developerguide/dynamodb-v2-rule.html) in the *AWS IoT Developer Guide\.*\.

`PutItem`  <a name="cfn-iot-topicrule-dynamodbv2action-putitem"></a>
Specifies the database table to which to write the item for an AWS IoT topic rule\.  
 *Required*: No  
 *Type*: [AWS IoT TopicRule PutItemInput](aws-properties-iot-topicrule-putiteminput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-iot-topicrule-dynamodbv2action-rolearn"></a>
The IAM role that allows access to the DynamoDB table\. At a minimum, the role must allow the `dynamoDB:PutItem` IAM action\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 