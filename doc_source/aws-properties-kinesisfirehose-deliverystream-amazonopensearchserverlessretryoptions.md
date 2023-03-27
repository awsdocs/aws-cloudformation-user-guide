# AWS::KinesisFirehose::DeliveryStream AmazonOpenSearchServerlessRetryOptions<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions"></a>

Configures retry behavior in case Kinesis Data Firehose is unable to deliver documents to the Serverless offering for Amazon OpenSearch Service\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions-syntax.json"></a>

```
{
  "[DurationInSeconds](#cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions-durationinseconds)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions-syntax.yaml"></a>

```
  [DurationInSeconds](#cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions-durationinseconds): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions-properties"></a>

`DurationInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessretryoptions-durationinseconds"></a>
After an initial failure to deliver to the Serverless offering for Amazon OpenSearch Service, the total amount of time during which Kinesis Data Firehose retries delivery \(including the first attempt\)\. After this time has elapsed, the failed documents are written to Amazon S3\. Default value is 300 seconds \(5 minutes\)\. A value of 0 \(zero\) results in no retries\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `7200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)