# AWS::IoTEvents::DetectorModel Action<a name="aws-properties-iotevents-detectormodel-action"></a>

An action to be performed when the `"condition"` is TRUE\.

## Syntax<a name="aws-properties-iotevents-detectormodel-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-action-syntax.json"></a>

```
{
  "[ClearTimer](#cfn-iotevents-detectormodel-action-cleartimer)" : [ClearTimer](aws-properties-iotevents-detectormodel-cleartimer.md),
  "[Firehose](#cfn-iotevents-detectormodel-action-firehose)" : [Firehose](aws-properties-iotevents-detectormodel-firehose.md),
  "[IotEvents](#cfn-iotevents-detectormodel-action-iotevents)" : [IotEvents](aws-properties-iotevents-detectormodel-iotevents.md),
  "[IotTopicPublish](#cfn-iotevents-detectormodel-action-iottopicpublish)" : [IotTopicPublish](aws-properties-iotevents-detectormodel-iottopicpublish.md),
  "[Lambda](#cfn-iotevents-detectormodel-action-lambda)" : [Lambda](aws-properties-iotevents-detectormodel-lambda.md),
  "[ResetTimer](#cfn-iotevents-detectormodel-action-resettimer)" : [ResetTimer](aws-properties-iotevents-detectormodel-resettimer.md),
  "[SetTimer](#cfn-iotevents-detectormodel-action-settimer)" : [SetTimer](aws-properties-iotevents-detectormodel-settimer.md),
  "[SetVariable](#cfn-iotevents-detectormodel-action-setvariable)" : [SetVariable](aws-properties-iotevents-detectormodel-setvariable.md),
  "[Sns](#cfn-iotevents-detectormodel-action-sns)" : [Sns](aws-properties-iotevents-detectormodel-sns.md),
  "[Sqs](#cfn-iotevents-detectormodel-action-sqs)" : [Sqs](aws-properties-iotevents-detectormodel-sqs.md)
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-action-syntax.yaml"></a>

```
  [ClearTimer](#cfn-iotevents-detectormodel-action-cleartimer): 
    [ClearTimer](aws-properties-iotevents-detectormodel-cleartimer.md)
  [Firehose](#cfn-iotevents-detectormodel-action-firehose): 
    [Firehose](aws-properties-iotevents-detectormodel-firehose.md)
  [IotEvents](#cfn-iotevents-detectormodel-action-iotevents): 
    [IotEvents](aws-properties-iotevents-detectormodel-iotevents.md)
  [IotTopicPublish](#cfn-iotevents-detectormodel-action-iottopicpublish): 
    [IotTopicPublish](aws-properties-iotevents-detectormodel-iottopicpublish.md)
  [Lambda](#cfn-iotevents-detectormodel-action-lambda): 
    [Lambda](aws-properties-iotevents-detectormodel-lambda.md)
  [ResetTimer](#cfn-iotevents-detectormodel-action-resettimer): 
    [ResetTimer](aws-properties-iotevents-detectormodel-resettimer.md)
  [SetTimer](#cfn-iotevents-detectormodel-action-settimer): 
    [SetTimer](aws-properties-iotevents-detectormodel-settimer.md)
  [SetVariable](#cfn-iotevents-detectormodel-action-setvariable): 
    [SetVariable](aws-properties-iotevents-detectormodel-setvariable.md)
  [Sns](#cfn-iotevents-detectormodel-action-sns): 
    [Sns](aws-properties-iotevents-detectormodel-sns.md)
  [Sqs](#cfn-iotevents-detectormodel-action-sqs): 
    [Sqs](aws-properties-iotevents-detectormodel-sqs.md)
```

## Properties<a name="aws-properties-iotevents-detectormodel-action-properties"></a>

`ClearTimer`  <a name="cfn-iotevents-detectormodel-action-cleartimer"></a>
Information needed to clear the timer\.  
*Required*: No  
*Type*: [ClearTimer](aws-properties-iotevents-detectormodel-cleartimer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Firehose`  <a name="cfn-iotevents-detectormodel-action-firehose"></a>
Sends information about the detector model instance and the event which triggered the action to a Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: [Firehose](aws-properties-iotevents-detectormodel-firehose.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotEvents`  <a name="cfn-iotevents-detectormodel-action-iotevents"></a>
Sends an IoT Events input, passing in information about the detector model instance and the event which triggered the action\.  
*Required*: No  
*Type*: [IotEvents](aws-properties-iotevents-detectormodel-iotevents.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotTopicPublish`  <a name="cfn-iotevents-detectormodel-action-iottopicpublish"></a>
Publishes an MQTT message with the given topic to the AWS IoT message broker\.  
*Required*: No  
*Type*: [IotTopicPublish](aws-properties-iotevents-detectormodel-iottopicpublish.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lambda`  <a name="cfn-iotevents-detectormodel-action-lambda"></a>
Calls an AWS Lambda function, passing in information about the detector model instance and the event which triggered the action\.  
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
Sends information about the detector model instance and the event which triggered the action to an Amazon SQS queue\.  
*Required*: No  
*Type*: [Sqs](aws-properties-iotevents-detectormodel-sqs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)