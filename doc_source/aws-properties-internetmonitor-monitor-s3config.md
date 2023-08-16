# AWS::InternetMonitor::Monitor S3Config<a name="aws-properties-internetmonitor-monitor-s3config"></a>

The configuration for publishing Amazon CloudWatch Internet Monitor internet measurements to Amazon S3\. The configuration includes the bucket name and \(optionally\) bucket prefix for the S3 bucket to store the measurements, and the delivery status\. The delivery status is `ENABLED` if you choose to deliver internet measurements to S3 logs, and `DISABLED` otherwise\.

The measurements are also published to Amazon CloudWatch Logs\.

## Syntax<a name="aws-properties-internetmonitor-monitor-s3config-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-internetmonitor-monitor-s3config-syntax.json"></a>

```
{
  "[BucketName](#cfn-internetmonitor-monitor-s3config-bucketname)" : String,
  "[BucketPrefix](#cfn-internetmonitor-monitor-s3config-bucketprefix)" : String,
  "[LogDeliveryStatus](#cfn-internetmonitor-monitor-s3config-logdeliverystatus)" : String
}
```

### YAML<a name="aws-properties-internetmonitor-monitor-s3config-syntax.yaml"></a>

```
  [BucketName](#cfn-internetmonitor-monitor-s3config-bucketname): String
  [BucketPrefix](#cfn-internetmonitor-monitor-s3config-bucketprefix): String
  [LogDeliveryStatus](#cfn-internetmonitor-monitor-s3config-logdeliverystatus): String
```

## Properties<a name="aws-properties-internetmonitor-monitor-s3config-properties"></a>

`BucketName`  <a name="cfn-internetmonitor-monitor-s3config-bucketname"></a>
The Amazon S3 bucket name for internet measurements publishing\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketPrefix`  <a name="cfn-internetmonitor-monitor-s3config-bucketprefix"></a>
An optional Amazon S3 bucket prefix for internet measurements publishing\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogDeliveryStatus`  <a name="cfn-internetmonitor-monitor-s3config-logdeliverystatus"></a>
The status of publishing Internet Monitor internet measurements to an Amazon S3 bucket\. The delivery status is `ENABLED` if you choose to deliver internet measurements to an S3 bucket, and `DISABLED` otherwise\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)