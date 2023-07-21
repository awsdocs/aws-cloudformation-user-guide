# AWS::InternetMonitor::Monitor S3Config<a name="aws-properties-internetmonitor-monitor-s3config"></a>

Configuration information for other locations that you choose to publish Amazon CloudWatch Internet Monitor internet measurements to, such as Amazon S3\. The measurements are also published to Amazon CloudWatch Logs\.

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
The Amazon S3 bucket name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketPrefix`  <a name="cfn-internetmonitor-monitor-s3config-bucketprefix"></a>
The Amazon S3 bucket prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogDeliveryStatus`  <a name="cfn-internetmonitor-monitor-s3config-logdeliverystatus"></a>
The status of publishing Internet Monitor internet measurements to an Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)