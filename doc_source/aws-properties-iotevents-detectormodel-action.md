# AWS::IoTEvents::DetectorModel Action<a name="aws-properties-iotevents-detectormodel-action"></a>

An action to be performed when the `condition` is TRUE\.

## Syntax<a name="aws-properties-iotevents-detectormodel-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-action-syntax.json"></a>

```
{
  "[ClearTimer](#cfn-iotevents-detectormodel-action-cleartimer)" : ClearTimer,
  "[DynamoDB](#cfn-iotevents-detectormodel-action-dynamodb)" : DynamoDB,
  "[DynamoDBv2](#cfn-iotevents-detectormodel-action-dynamodbv2)" : DynamoDBv2,
  "[Firehose](#cfn-iotevents-detectormodel-action-firehose)" : Firehose,
  "[IotEvents](#cfn-iotevents-detectormodel-action-iotevents)" : IotEvents,
  "[IotSiteWise](#cfn-iotevents-detectormodel-action-iotsitewise)" : IotSiteWise,
  "[IotTopicPublish](#cfn-iotevents-detectormodel-action-iottopicpublish)" : IotTopicPublish,
  "[Lambda](#cfn-iotevents-detectormodel-action-lambda)" : Lambda,
  "[ResetTimer](#cfn-iotevents-detectormodel-action-resettimer)" : ResetTimer,
  "[SetTimer](#cfn-iotevents-detectormodel-action-settimer)" : SetTimer,
  "[SetVariable](#cfn-iotevents-detectormodel-action-setvariable)" : SetVariable,
  "[Sns](#cfn-iotevents-detectormodel-action-sns)" : Sns,
  "[Sqs](#cfn-iotevents-detectormodel-action-sqs)" : Sqs
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-action-syntax.yaml"></a>

```
  [ClearTimer](#cfn-iotevents-detectormodel-action-cleartimer): 
    ClearTimer
  [DynamoDB](#cfn-iotevents-detectormodel-action-dynamodb): 
    DynamoDB
  [DynamoDBv2](#cfn-iotevents-detectormodel-action-dynamodbv2): 
    DynamoDBv2
  [Firehose](#cfn-iotevents-detectormodel-action-firehose): 
    Firehose
  [IotEvents](#cfn-iotevents-detectormodel-action-iotevents): 
    IotEvents
  [IotSiteWise](#cfn-iotevents-detectormodel-action-iotsitewise): 
    IotSiteWise
  [IotTopicPublish](#cfn-iotevents-detectormodel-action-iottopicpublish): 
    IotTopicPublish
  [Lambda](#cfn-iotevents-detectormodel-action-lambda): 
    Lambda
  [ResetTimer](#cfn-iotevents-detectormodel-action-resettimer): 
    ResetTimer
  [SetTimer](#cfn-iotevents-detectormodel-action-settimer): 
    SetTimer
  [SetVariable](#cfn-iotevents-detectormodel-action-setvariable): 
    SetVariable
  [Sns](#cfn-iotevents-detectormodel-action-sns): 
    Sns
  [Sqs](#cfn-iotevents-detectormodel-action-sqs): 
    Sqs
```

## Properties<a name="aws-properties-iotevents-detectormodel-action-properties"></a>

`ClearTimer`  <a name="cfn-iotevents-detectormodel-action-cleartimer"></a>
Information needed to clear the timer\.  
*Required*: No  
*Type*: [ClearTimer](aws-properties-iotevents-detectormodel-cleartimer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDB`  <a name="cfn-iotevents-detectormodel-action-dynamodb"></a>
Writes to the DynamoDB table that you created\. The default action payload contains all attribute\-value pairs that have the information about the detector model instance and the event that triggered the action\. You can customize the [payload](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Payload.html)\. One column of the DynamoDB table receives all attribute\-value pairs in the payload that you specify\. For more information, see [Actions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-event-actions.html) in *AWS IoT Events Developer Guide*\.  
*Required*: No  
*Type*: [DynamoDB](aws-properties-iotevents-detectormodel-dynamodb.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDBv2`  <a name="cfn-iotevents-detectormodel-action-dynamodbv2"></a>
Writes to the DynamoDB table that you created\. The default action payload contains all attribute\-value pairs that have the information about the detector model instance and the event that triggered the action\. You can customize the [payload](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Payload.html)\. A separate column of the DynamoDB table receives one attribute\-value pair in the payload that you specify\. For more information, see [Actions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-event-actions.html) in *AWS IoT Events Developer Guide*\.  
*Required*: No  
*Type*: [DynamoDBv2](aws-properties-iotevents-detectormodel-dynamodbv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Firehose`  <a name="cfn-iotevents-detectormodel-action-firehose"></a>
Sends information about the detector model instance and the event that triggered the action to an Amazon Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: [Firehose](aws-properties-iotevents-detectormodel-firehose.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotEvents`  <a name="cfn-iotevents-detectormodel-action-iotevents"></a>
Sends AWS IoT Events input, which passes information about the detector model instance and the event that triggered the action\.  
*Required*: No  
*Type*: [IotEvents](aws-properties-iotevents-detectormodel-iotevents.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotSiteWise`  <a name="cfn-iotevents-detectormodel-action-iotsitewise"></a>
Sends information about the detector model instance and the event that triggered the action to an asset property in AWS IoT SiteWise \.  
*Required*: No  
*Type*: [IotSiteWise](aws-properties-iotevents-detectormodel-iotsitewise.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotTopicPublish`  <a name="cfn-iotevents-detectormodel-action-iottopicpublish"></a>
Publishes an MQTT message with the given topic to the AWS IoT message broker\.  
*Required*: No  
*Type*: [IotTopicPublish](aws-properties-iotevents-detectormodel-iottopicpublish.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lambda`  <a name="cfn-iotevents-detectormodel-action-lambda"></a>
Calls a Lambda function, passing in information about the detector model instance and the event that triggered the action\.  
*Required*: No  
*Type*: [Lambda](aws-properties-iotevents-detectormodel-lambda.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResetTimer`  <a name="cfn-iotevents-detectormodel-action-resettimer"></a>
Information needed to reset the timer\.  
*Required*: No  
*Type*: [ResetTimer](aws-properties-iotevents-detectormodel-resettimer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SetTimer`  <a name="cfn-iotevents-detectormodel-action-settimer"></a>
Information needed to set the timer\.  
*Required*: No  
*Type*: [SetTimer](aws-properties-iotevents-detectormodel-settimer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SetVariable`  <a name="cfn-iotevents-detectormodel-action-setvariable"></a>
Sets a variable to a specified value\.  
*Required*: No  
*Type*: [SetVariable](aws-properties-iotevents-detectormodel-setvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sns`  <a name="cfn-iotevents-detectormodel-action-sns"></a>
Sends an Amazon SNS message\.  
*Required*: No  
*Type*: [Sns](aws-properties-iotevents-detectormodel-sns.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sqs`  <a name="cfn-iotevents-detectormodel-action-sqs"></a>
Sends an Amazon SNS message\.  
*Required*: No  
*Type*: [Sqs](aws-properties-iotevents-detectormodel-sqs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)