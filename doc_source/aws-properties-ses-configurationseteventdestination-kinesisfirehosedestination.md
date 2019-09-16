# AWS::SES::ConfigurationSetEventDestination KinesisFirehoseDestination<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination"></a>

Contains the delivery stream ARN and the IAM role ARN associated with an Amazon Kinesis Data Firehose event destination\.

Event destinations, such as Amazon Kinesis Data Firehose, are associated with configuration sets, which enable you to publish email sending events\. For information about using configuration sets, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/monitor-sending-activity.html)\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-syntax.json"></a>

```
{
  "[DeliveryStreamARN](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn)" : String,
  "[IAMRoleARN](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-iamrolearn)" : String
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-syntax.yaml"></a>

```
  [DeliveryStreamARN](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn): String
  [IAMRoleARN](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-iamrolearn): String
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-properties"></a>

`DeliveryStreamARN`  <a name="cfn-ses-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn"></a>
The ARN of the Amazon Kinesis Data Firehose stream that email sending events should be published to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IAMRoleARN`  <a name="cfn-ses-configurationseteventdestination-kinesisfirehosedestination-iamrolearn"></a>
The ARN of the IAM role that Amazon SES uses to publish email sending events to the Amazon Kinesis Data Firehose stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)