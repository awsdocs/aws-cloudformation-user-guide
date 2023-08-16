# AWS::Rekognition::StreamProcessor NotificationChannel<a name="aws-properties-rekognition-streamprocessor-notificationchannel"></a>

 The Amazon Simple Notification Service topic to which Amazon Rekognition publishes the object detection results and completion status of a video analysis operation\. Amazon Rekognition publishes a notification the first time an object of interest or a person is detected in the video stream\. Amazon Rekognition also publishes an an end\-of\-session notification with a summary when the stream processing session is complete\. For more information, see [StreamProcessorNotificationChannel](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_StreamProcessorNotificationChannel)\.

## Syntax<a name="aws-properties-rekognition-streamprocessor-notificationchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rekognition-streamprocessor-notificationchannel-syntax.json"></a>

```
{
  "[Arn](#cfn-rekognition-streamprocessor-notificationchannel-arn)" : String
}
```

### YAML<a name="aws-properties-rekognition-streamprocessor-notificationchannel-syntax.yaml"></a>

```
  [Arn](#cfn-rekognition-streamprocessor-notificationchannel-arn): String
```

## Properties<a name="aws-properties-rekognition-streamprocessor-notificationchannel-properties"></a>

`Arn`  <a name="cfn-rekognition-streamprocessor-notificationchannel-arn"></a>
The ARN of the SNS topic that receives notifications\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)