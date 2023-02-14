# AWS::IoT::TopicRule DynamoDBv2Action<a name="aws-properties-iot-topicrule-dynamodbv2action"></a>

Describes an action to write to a DynamoDB table\.

This DynamoDB action writes each attribute in the message payload into it's own column in the DynamoDB table\.

## Syntax<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax.json"></a>

```
{
  "[PutItem](#cfn-iot-topicrule-dynamodbv2action-putitem)" : PutItemInput,
  "[RoleArn](#cfn-iot-topicrule-dynamodbv2action-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-dynamodbv2action-syntax.yaml"></a>

```
  [PutItem](#cfn-iot-topicrule-dynamodbv2action-putitem): 
    PutItemInput
  [RoleArn](#cfn-iot-topicrule-dynamodbv2action-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-dynamodbv2action-properties"></a>

`PutItem`  <a name="cfn-iot-topicrule-dynamodbv2action-putitem"></a>
Specifies the DynamoDB table to which the message data will be written\. For example:  
 `{ "dynamoDBv2": { "roleArn": "aws:iam:12341251:my-role" "putItem": { "tableName": "my-table" } } }`   
Each attribute in the message payload will be written to a separate column in the DynamoDB database\.  
*Required*: No  
*Type*: [PutItemInput](aws-properties-iot-topicrule-putiteminput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-dynamodbv2action-rolearn"></a>
The ARN of the IAM role that grants access to the DynamoDB table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-iot-topicrule-dynamodbv2action--seealso"></a>
+  [AWS SDK for C\+\+](https://sdk.amazonaws.com/cpp/api/LATEST/class_aws_1_1_io_t_1_1_model_1_1_dynamo_d_bv2_action.html)\.
+  [AWS SDK for Go](https://docs.aws.amazon.com/sdk-for-go/api/service/iot/#DynamoDBv2Action)\.
+  [AWS SDK for Java](https://docs.aws.amazon.com/AWSJavaSDK/latest/javadoc/com/amazonaws/services/iot/model/DynamoDBv2Action.html)\.
+  [AWS SDK for Ruby V2](https://docs.aws.amazon.com/sdkforruby/api/Aws/IoT/Types/DynamoDBv2Action.html)\.

