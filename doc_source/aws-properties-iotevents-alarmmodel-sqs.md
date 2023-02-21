# AWS::IoTEvents::AlarmModel Sqs<a name="aws-properties-iotevents-alarmmodel-sqs"></a>

Sends information about the detector model instance and the event that triggered the action to an Amazon SQS queue\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-sqs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-sqs-syntax.json"></a>

```
{
  "[Payload](#cfn-iotevents-alarmmodel-sqs-payload)" : Payload,
  "[QueueUrl](#cfn-iotevents-alarmmodel-sqs-queueurl)" : String,
  "[UseBase64](#cfn-iotevents-alarmmodel-sqs-usebase64)" : Boolean
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-sqs-syntax.yaml"></a>

```
  [Payload](#cfn-iotevents-alarmmodel-sqs-payload): 
    Payload
  [QueueUrl](#cfn-iotevents-alarmmodel-sqs-queueurl): String
  [UseBase64](#cfn-iotevents-alarmmodel-sqs-usebase64): Boolean
```

## Properties<a name="aws-properties-iotevents-alarmmodel-sqs-properties"></a>

`Payload`  <a name="cfn-iotevents-alarmmodel-sqs-payload"></a>
You can configure the action payload when you send a message to an Amazon SQS queue\.  
*Required*: No  
*Type*: [Payload](aws-properties-iotevents-alarmmodel-payload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueUrl`  <a name="cfn-iotevents-alarmmodel-sqs-queueurl"></a>
The URL of the SQS queue where the data is written\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseBase64`  <a name="cfn-iotevents-alarmmodel-sqs-usebase64"></a>
Set this to TRUE if you want the data to be base\-64 encoded before it is written to the queue\. Otherwise, set this to FALSE\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)