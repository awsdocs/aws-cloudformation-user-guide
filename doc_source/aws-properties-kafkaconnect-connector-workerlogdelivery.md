# AWS::KafkaConnect::Connector WorkerLogDelivery<a name="aws-properties-kafkaconnect-connector-workerlogdelivery"></a>

Workers can send worker logs to different destination types\. This configuration specifies the details of these destinations\.

## Syntax<a name="aws-properties-kafkaconnect-connector-workerlogdelivery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-workerlogdelivery-syntax.json"></a>

```
{
  "[CloudWatchLogs](#cfn-kafkaconnect-connector-workerlogdelivery-cloudwatchlogs)" : CloudWatchLogsLogDelivery,
  "[Firehose](#cfn-kafkaconnect-connector-workerlogdelivery-firehose)" : FirehoseLogDelivery,
  "[S3](#cfn-kafkaconnect-connector-workerlogdelivery-s3)" : S3LogDelivery
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-workerlogdelivery-syntax.yaml"></a>

```
  [CloudWatchLogs](#cfn-kafkaconnect-connector-workerlogdelivery-cloudwatchlogs): 
    CloudWatchLogsLogDelivery
  [Firehose](#cfn-kafkaconnect-connector-workerlogdelivery-firehose): 
    FirehoseLogDelivery
  [S3](#cfn-kafkaconnect-connector-workerlogdelivery-s3): 
    S3LogDelivery
```

## Properties<a name="aws-properties-kafkaconnect-connector-workerlogdelivery-properties"></a>

`CloudWatchLogs`  <a name="cfn-kafkaconnect-connector-workerlogdelivery-cloudwatchlogs"></a>
Details about delivering logs to Amazon CloudWatch Logs\.  
*Required*: No  
*Type*: [CloudWatchLogsLogDelivery](aws-properties-kafkaconnect-connector-cloudwatchlogslogdelivery.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Firehose`  <a name="cfn-kafkaconnect-connector-workerlogdelivery-firehose"></a>
Details about delivering logs to Amazon Kinesis Data Firehose\.  
*Required*: No  
*Type*: [FirehoseLogDelivery](aws-properties-kafkaconnect-connector-firehoselogdelivery.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3`  <a name="cfn-kafkaconnect-connector-workerlogdelivery-s3"></a>
Details about delivering logs to Amazon S3\.  
*Required*: No  
*Type*: [S3LogDelivery](aws-properties-kafkaconnect-connector-s3logdelivery.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)