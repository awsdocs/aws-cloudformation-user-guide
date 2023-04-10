# AWS::InternetMonitor::Monitor InternetMeasurementsLogDelivery<a name="aws-properties-internetmonitor-monitor-internetmeasurementslogdelivery"></a>

The internet measurements for Amazon CloudWatch Internet Monitor published to another location, such as an Amazon S3 bucket\. Measurements are automatically published to Amazon CloudWatch Logs for the top 500 city\-networks \(by traffic volume\)\.

## Syntax<a name="aws-properties-internetmonitor-monitor-internetmeasurementslogdelivery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-internetmonitor-monitor-internetmeasurementslogdelivery-syntax.json"></a>

```
{
  "[S3Config](#cfn-internetmonitor-monitor-internetmeasurementslogdelivery-s3config)" : S3Config
}
```

### YAML<a name="aws-properties-internetmonitor-monitor-internetmeasurementslogdelivery-syntax.yaml"></a>

```
  [S3Config](#cfn-internetmonitor-monitor-internetmeasurementslogdelivery-s3config): 
    S3Config
```

## Properties<a name="aws-properties-internetmonitor-monitor-internetmeasurementslogdelivery-properties"></a>

`S3Config`  <a name="cfn-internetmonitor-monitor-internetmeasurementslogdelivery-s3config"></a>
The configuration information for publishing Amazon CloudWatch Internet Monitor internet measurements to Amazon S3\. The configuration includes the bucket name and \(optionally\) bucket prefix for the S3 bucket to store the measurements, and the delivery status\. The delivery status is `ENABLED` if you choose to deliver internet measurements to an S3 bucket, and `DISABLED` otherwise\.  
*Required*: No  
*Type*: [S3Config](aws-properties-internetmonitor-monitor-s3config.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)