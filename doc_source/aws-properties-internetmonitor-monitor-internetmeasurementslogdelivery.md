# AWS::InternetMonitor::Monitor InternetMeasurementsLogDelivery<a name="aws-properties-internetmonitor-monitor-internetmeasurementslogdelivery"></a>

Publish internet measurements to an Amazon S3 bucket in addition to CloudWatch Logs\.

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
The Amazon S3 bucket where you publish internet measurements in addition to CloudWatch Logs\.  
*Required*: No  
*Type*: [S3Config](aws-properties-internetmonitor-monitor-s3config.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)