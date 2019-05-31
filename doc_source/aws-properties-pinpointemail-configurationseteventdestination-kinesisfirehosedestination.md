# AWS::PinpointEmail::ConfigurationSetEventDestination KinesisFirehoseDestination<a name="aws-properties-pinpointemail-configurationseteventdestination-kinesisfirehosedestination"></a>

An object that defines an Amazon Kinesis Data Firehose destination for email events\. You can use Amazon Kinesis Data Firehose to stream data to other services, such as Amazon S3 and Amazon Redshift\.

## Syntax<a name="aws-properties-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-syntax.json"></a>

```
{
  "[DeliveryStreamArn](#cfn-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn)" : String,
  "[IamRoleArn](#cfn-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-iamrolearn)" : String
}
```

### YAML<a name="aws-properties-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-syntax.yaml"></a>

```
  [DeliveryStreamArn](#cfn-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn): String
  [IamRoleArn](#cfn-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-iamrolearn): String
```

## Properties<a name="aws-properties-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-properties"></a>

`DeliveryStreamArn`  <a name="cfn-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Kinesis Data Firehose stream that Amazon Pinpoint sends email events to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRoleArn`  <a name="cfn-pinpointemail-configurationseteventdestination-kinesisfirehosedestination-iamrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that Amazon Pinpoint uses when sending email events to the Amazon Kinesis Data Firehose stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)