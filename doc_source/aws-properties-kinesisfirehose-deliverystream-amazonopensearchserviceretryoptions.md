# AWS::KinesisFirehose::DeliveryStream AmazonopensearchserviceRetryOptions<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions"></a>

Configures retry behavior in case Kinesis Data Firehose is unable to deliver documents to Amazon OpenSearch Service\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions-syntax.json"></a>

```
{
  "[DurationInSeconds](#cfn-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions-durationinseconds)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions-syntax.yaml"></a>

```
  [DurationInSeconds](#cfn-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions-durationinseconds): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions-properties"></a>

`DurationInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions-durationinseconds"></a>
After an initial failure to deliver to Amazon OpenSearch Service, the total amount of time during which Kinesis Data Firehose retries delivery \(including the first attempt\)\. After this time has elapsed, the failed documents are written to Amazon S3\. Default value is 300 seconds \(5 minutes\)\. A value of 0 \(zero\) results in no retries\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `7200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)