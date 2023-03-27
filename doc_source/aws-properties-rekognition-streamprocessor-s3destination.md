# AWS::Rekognition::StreamProcessor S3Destination<a name="aws-properties-rekognition-streamprocessor-s3destination"></a>

The Amazon S3 bucket location to which Amazon Rekognition publishes the detailed inference results of a video analysis operation\. These results include the name of the stream processor resource, the session ID of the stream processing session, and labeled timestamps and bounding boxes for detected labels\. For more information, see [S3Destination](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_S3Destination)\.

## Syntax<a name="aws-properties-rekognition-streamprocessor-s3destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rekognition-streamprocessor-s3destination-syntax.json"></a>

```
{
  "[BucketName](#cfn-rekognition-streamprocessor-s3destination-bucketname)" : String,
  "[ObjectKeyPrefix](#cfn-rekognition-streamprocessor-s3destination-objectkeyprefix)" : String
}
```

### YAML<a name="aws-properties-rekognition-streamprocessor-s3destination-syntax.yaml"></a>

```
  [BucketName](#cfn-rekognition-streamprocessor-s3destination-bucketname): String
  [ObjectKeyPrefix](#cfn-rekognition-streamprocessor-s3destination-objectkeyprefix): String
```

## Properties<a name="aws-properties-rekognition-streamprocessor-s3destination-properties"></a>

`BucketName`  <a name="cfn-rekognition-streamprocessor-s3destination-bucketname"></a>
Describes the destination Amazon Simple Storage Service \(Amazon S3\) bucket name of a stream processor's exports\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ObjectKeyPrefix`  <a name="cfn-rekognition-streamprocessor-s3destination-objectkeyprefix"></a>
Describes the destination Amazon Simple Storage Service \(Amazon S3\) object keys of a stream processor's exports\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)