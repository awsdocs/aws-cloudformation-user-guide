# AWS::Rekognition::StreamProcessor KinesisVideoStream<a name="aws-properties-rekognition-streamprocessor-kinesisvideostream"></a>

The Kinesis video stream that provides the source of the streaming video for an Amazon Rekognition Video stream processor\. For more information, see [KinesisVideoStream](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_KinesisVideoStream)\.

## Syntax<a name="aws-properties-rekognition-streamprocessor-kinesisvideostream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rekognition-streamprocessor-kinesisvideostream-syntax.json"></a>

```
{
  "[Arn](#cfn-rekognition-streamprocessor-kinesisvideostream-arn)" : String
}
```

### YAML<a name="aws-properties-rekognition-streamprocessor-kinesisvideostream-syntax.yaml"></a>

```
  [Arn](#cfn-rekognition-streamprocessor-kinesisvideostream-arn): String
```

## Properties<a name="aws-properties-rekognition-streamprocessor-kinesisvideostream-properties"></a>

`Arn`  <a name="cfn-rekognition-streamprocessor-kinesisvideostream-arn"></a>
ARN of the Kinesis video stream stream that streams the source video\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `(^arn:([a-z\d-]+):kinesisvideo:([a-z\d-]+):\d{12}:.+$)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)