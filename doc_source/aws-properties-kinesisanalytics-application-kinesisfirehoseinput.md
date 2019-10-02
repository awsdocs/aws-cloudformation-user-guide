# AWS::KinesisAnalytics::Application KinesisFirehoseInput<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput"></a>

 Identifies an Amazon Kinesis Firehose delivery stream as the streaming source\. You provide the delivery stream's Amazon Resource Name \(ARN\) and an IAM role ARN that enables Amazon Kinesis Analytics to access the stream on your behalf\.

## Syntax<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalytics-application-kinesisfirehoseinput-resourcearn)" : String,
  "[RoleARN](#cfn-kinesisanalytics-application-kinesisfirehoseinput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalytics-application-kinesisfirehoseinput-resourcearn): String
  [RoleARN](#cfn-kinesisanalytics-application-kinesisfirehoseinput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalytics-application-kinesisfirehoseinput-resourcearn"></a>
ARN of the input delivery stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisanalytics-application-kinesisfirehoseinput-rolearn"></a>
ARN of the IAM role that Amazon Kinesis Analytics can assume to access the stream on your behalf\. You need to make sure that the role has the necessary permissions to access the stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:aws:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
