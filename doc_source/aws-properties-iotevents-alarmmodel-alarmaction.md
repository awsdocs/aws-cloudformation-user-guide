# AWS::IoTEvents::AlarmModel AlarmAction<a name="aws-properties-iotevents-alarmmodel-alarmaction"></a>

Specifies one of the following actions to receive notifications when the alarm state changes\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-alarmaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-alarmaction-syntax.json"></a>

```
{
  "[DynamoDB](#cfn-iotevents-alarmmodel-alarmaction-dynamodb)" : DynamoDB,
  "[DynamoDBv2](#cfn-iotevents-alarmmodel-alarmaction-dynamodbv2)" : DynamoDBv2,
  "[Firehose](#cfn-iotevents-alarmmodel-alarmaction-firehose)" : Firehose,
  "[IotEvents](#cfn-iotevents-alarmmodel-alarmaction-iotevents)" : IotEvents,
  "[IotSiteWise](#cfn-iotevents-alarmmodel-alarmaction-iotsitewise)" : IotSiteWise,
  "[IotTopicPublish](#cfn-iotevents-alarmmodel-alarmaction-iottopicpublish)" : IotTopicPublish,
  "[Lambda](#cfn-iotevents-alarmmodel-alarmaction-lambda)" : Lambda,
  "[Sns](#cfn-iotevents-alarmmodel-alarmaction-sns)" : Sns,
  "[Sqs](#cfn-iotevents-alarmmodel-alarmaction-sqs)" : Sqs
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-alarmaction-syntax.yaml"></a>

```
  [DynamoDB](#cfn-iotevents-alarmmodel-alarmaction-dynamodb): 
    DynamoDB
  [DynamoDBv2](#cfn-iotevents-alarmmodel-alarmaction-dynamodbv2): 
    DynamoDBv2
  [Firehose](#cfn-iotevents-alarmmodel-alarmaction-firehose): 
    Firehose
  [IotEvents](#cfn-iotevents-alarmmodel-alarmaction-iotevents): 
    IotEvents
  [IotSiteWise](#cfn-iotevents-alarmmodel-alarmaction-iotsitewise): 
    IotSiteWise
  [IotTopicPublish](#cfn-iotevents-alarmmodel-alarmaction-iottopicpublish): 
    IotTopicPublish
  [Lambda](#cfn-iotevents-alarmmodel-alarmaction-lambda): 
    Lambda
  [Sns](#cfn-iotevents-alarmmodel-alarmaction-sns): 
    Sns
  [Sqs](#cfn-iotevents-alarmmodel-alarmaction-sqs): 
    Sqs
```

## Properties<a name="aws-properties-iotevents-alarmmodel-alarmaction-properties"></a>

`DynamoDB`  <a name="cfn-iotevents-alarmmodel-alarmaction-dynamodb"></a>
Defines an action to write to the Amazon DynamoDB table that you created\. The standard action payload contains all the information about the detector model instance and the event that triggered the action\. You can customize the [payload](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Payload.html)\. One column of the DynamoDB table receives all attribute\-value pairs in the payload that you specify\.  
You must use expressions for all parameters in `DynamoDBAction`\. The expressions accept literals, operators, functions, references, and substitution templates\.  

**Examples**
+ For literal values, the expressions must contain single quotes\. For example, the value for the `hashKeyType` parameter can be `'STRING'`\.
+ For references, you must specify either variables or input values\. For example, the value for the `hashKeyField` parameter can be `$input.GreenhouseInput.name`\.
+ For a substitution template, you must use `${}`, and the template must be in single quotes\. A substitution template can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `hashKeyValue` parameter uses a substitution template\. 

   `'${$input.GreenhouseInput.temperature * 6 / 5 + 32} in Fahrenheit'` 
+ For a string concatenation, you must use `+`\. A string concatenation can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `tableName` parameter uses a string concatenation\. 

   `'GreenhouseTemperatureTable ' + $input.GreenhouseInput.date` 
For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the * AWS IoT Events Developer Guide*\.  
If the defined payload type is a string, `DynamoDBAction` writes non\-JSON data to the DynamoDB table as binary data\. The DynamoDB console displays the data as Base64\-encoded text\. The value for the `payloadField` parameter is `<payload-field>_raw`\.  
*Required*: No  
*Type*: [DynamoDB](aws-properties-iotevents-alarmmodel-dynamodb.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDBv2`  <a name="cfn-iotevents-alarmmodel-alarmaction-dynamodbv2"></a>
Defines an action to write to the Amazon DynamoDB table that you created\. The default action payload contains all the information about the detector model instance and the event that triggered the action\. You can customize the [payload](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Payload.html)\. A separate column of the DynamoDB table receives one attribute\-value pair in the payload that you specify\.  
You must use expressions for all parameters in `DynamoDBv2Action`\. The expressions accept literals, operators, functions, references, and substitution templates\.  

**Examples**
+ For literal values, the expressions must contain single quotes\. For example, the value for the `tableName` parameter can be `'GreenhouseTemperatureTable'`\.
+ For references, you must specify either variables or input values\. For example, the value for the `tableName` parameter can be `$variable.ddbtableName`\.
+ For a substitution template, you must use `${}`, and the template must be in single quotes\. A substitution template can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `contentExpression` parameter in `Payload` uses a substitution template\. 

   `'{\"sensorID\": \"${$input.GreenhouseInput.sensor_id}\", \"temperature\": \"${$input.GreenhouseInput.temperature * 9 / 5 + 32}\"}'` 
+ For a string concatenation, you must use `+`\. A string concatenation can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `tableName` parameter uses a string concatenation\. 

   `'GreenhouseTemperatureTable ' + $input.GreenhouseInput.date` 
For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the * AWS IoT Events Developer Guide*\.  
The value for the `type` parameter in `Payload` must be `JSON`\.  
*Required*: No  
*Type*: [DynamoDBv2](aws-properties-iotevents-alarmmodel-dynamodbv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Firehose`  <a name="cfn-iotevents-alarmmodel-alarmaction-firehose"></a>
Sends information about the detector model instance and the event that triggered the action to an Amazon Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: [Firehose](aws-properties-iotevents-alarmmodel-firehose.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotEvents`  <a name="cfn-iotevents-alarmmodel-alarmaction-iotevents"></a>
Sends an AWS IoT Events input, passing in information about the detector model instance and the event that triggered the action\.  
*Required*: No  
*Type*: [IotEvents](aws-properties-iotevents-alarmmodel-iotevents.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotSiteWise`  <a name="cfn-iotevents-alarmmodel-alarmaction-iotsitewise"></a>
Sends information about the detector model instance and the event that triggered the action to a specified asset property in AWS IoT SiteWise\.  
You must use expressions for all parameters in `IotSiteWiseAction`\. The expressions accept literals, operators, functions, references, and substitutions templates\.  

**Examples**
+ For literal values, the expressions must contain single quotes\. For example, the value for the `propertyAlias` parameter can be `'/company/windfarm/3/turbine/7/temperature'`\.
+ For references, you must specify either variables or input values\. For example, the value for the `assetId` parameter can be `$input.TurbineInput.assetId1`\.
+ For a substitution template, you must use `${}`, and the template must be in single quotes\. A substitution template can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `propertyAlias` parameter uses a substitution template\. 

   `'company/windfarm/${$input.TemperatureInput.sensorData.windfarmID}/turbine/ ${$input.TemperatureInput.sensorData.turbineID}/temperature'` 
You must specify either `propertyAlias` or both `assetId` and `propertyId` to identify the target asset property in AWS IoT SiteWise\.  
For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the * AWS IoT Events Developer Guide*\.  
*Required*: No  
*Type*: [IotSiteWise](aws-properties-iotevents-alarmmodel-iotsitewise.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotTopicPublish`  <a name="cfn-iotevents-alarmmodel-alarmaction-iottopicpublish"></a>
Information required to publish the MQTT message through the AWS IoT message broker\.  
*Required*: No  
*Type*: [IotTopicPublish](aws-properties-iotevents-alarmmodel-iottopicpublish.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lambda`  <a name="cfn-iotevents-alarmmodel-alarmaction-lambda"></a>
Calls a Lambda function, passing in information about the detector model instance and the event that triggered the action\.  
*Required*: No  
*Type*: [Lambda](aws-properties-iotevents-alarmmodel-lambda.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sns`  <a name="cfn-iotevents-alarmmodel-alarmaction-sns"></a>
Property description not available\.  
*Required*: No  
*Type*: [Sns](aws-properties-iotevents-alarmmodel-sns.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sqs`  <a name="cfn-iotevents-alarmmodel-alarmaction-sqs"></a>
Sends information about the detector model instance and the event that triggered the action to an Amazon SQS queue\.  
*Required*: No  
*Type*: [Sqs](aws-properties-iotevents-alarmmodel-sqs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)