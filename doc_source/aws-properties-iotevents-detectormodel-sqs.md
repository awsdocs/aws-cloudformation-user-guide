# AWS::IoTEvents::DetectorModel Sqs<a name="aws-properties-iotevents-detectormodel-sqs"></a>

Sends information about the detector model instance and the event which triggered the action to an Amazon SQS queue\.

## Syntax<a name="aws-properties-iotevents-detectormodel-sqs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-sqs-syntax.json"></a>

```
{
  "[QueueUrl](#cfn-iotevents-detectormodel-sqs-queueurl)" : String,
  "[UseBase64](#cfn-iotevents-detectormodel-sqs-usebase64)" : Boolean
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-sqs-syntax.yaml"></a>

```
  [QueueUrl](#cfn-iotevents-detectormodel-sqs-queueurl): String
  [UseBase64](#cfn-iotevents-detectormodel-sqs-usebase64): Boolean
```

## Properties<a name="aws-properties-iotevents-detectormodel-sqs-properties"></a>

`QueueUrl`  <a name="cfn-iotevents-detectormodel-sqs-queueurl"></a>
The URL of the Amazon SQS queue where the data is written\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseBase64`  <a name="cfn-iotevents-detectormodel-sqs-usebase64"></a>
Set this to TRUE if you want the data to be Base\-64 encoded before it is written to the queue\. Otherwise, set this to FALSE\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)