# AWS::KinesisAnalyticsV2::Application ZeppelinMonitoringConfiguration<a name="aws-properties-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration"></a>

Describes configuration parameters for Amazon CloudWatch logging for a Kinesis Data Analytics Studio notebook\. For more information about CloudWatch logging, see [Monitoring](https://docs.aws.amazon.com/kinesisanalytics/latest/java/monitoring-overview.html)\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration-syntax.json"></a>

```
{
  "[LogLevel](#cfn-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration-loglevel)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration-syntax.yaml"></a>

```
  [LogLevel](#cfn-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration-loglevel): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration-properties"></a>

`LogLevel`  <a name="cfn-kinesisanalyticsv2-application-zeppelinmonitoringconfiguration-loglevel"></a>
The verbosity of the CloudWatch Logs for an application\. You can set it to `INFO`, `WARN`, `ERROR`, or `DEBUG`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DEBUG | ERROR | INFO | WARN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)