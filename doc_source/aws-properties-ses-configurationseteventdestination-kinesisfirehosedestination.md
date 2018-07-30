# Amazon Simple Email Service ConfigurationSetEventDestination KinesisFirehoseDestination<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination"></a>

<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-description"></a>The `KinesisFirehoseDestination` property type specifies the delivery stream Arn and the IAM role Arn associated with an Kinesis Firehose event destination for an Amazon SES configuration set\.

<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-inheritance"></a> `KinesisFirehoseDestination` is a property of the [Amazon SES ConfigurationSetEventDestination EventDestination](aws-properties-ses-configurationseteventdestination-eventdestination.md) property type\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-syntax.json"></a>

```
{
  "[IAMRoleArn](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-iamrolearn)" : String,
  "[DeliveryStreamArn](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn)" : String
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-syntax.yaml"></a>

```
[IAMRoleArn](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-iamrolearn): String
[DeliveryStreamArn](#cfn-ses-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn): String
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-properties"></a>

`IAMRoleArn`  <a name="cfn-ses-configurationseteventdestination-kinesisfirehosedestination-iamrolearn"></a>
The Arn of the IAM role under which Amazon SES publishes email sending events to the Amazon Kinesis Firehose stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DeliveryStreamArn`  <a name="cfn-ses-configurationseteventdestination-kinesisfirehosedestination-deliverystreamarn"></a>
The Arn of the Amazon Kinesis Firehose stream that email sending events should be published to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination-seealso"></a>
+ [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*
+ [KinesisFirehoseDestination](http://docs.aws.amazon.com/ses/latest/APIReference/API_KinesisFirehoseDestination.html) in the *Amazon Simple Email Service API Reference*