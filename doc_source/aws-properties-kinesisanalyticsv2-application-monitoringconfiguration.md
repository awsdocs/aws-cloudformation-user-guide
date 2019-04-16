# Amazon Kinesis Data Analytics Application MonitoringConfiguration<a name="aws-properties-kinesisanalyticsv2-application-monitoringconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-monitoringconfiguration-description"></a>The `MonitoringConfiguration` property type specifies configuration parameters for Amazon CloudWatch logging for a Java\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-monitoringconfiguration-inheritance"></a> `MonitoringConfiguration` is a property of the [FlinkApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration.md) resource\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-monitoringconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-monitoringconfiguration-syntax.json"></a>

```
{
  "[ConfigurationType](#cfn-kinesisanalyticsv2-application-monitoringconfiguration-configurationtype)" : String,
  "[MetricsLevel](#cfn-kinesisanalyticsv2-application-monitoringconfiguration-metricslevel)" : String,
  "[LogLevel](#cfn-kinesisanalyticsv2-application-monitoringconfiguration-loglevel)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-monitoringconfiguration-syntax.yaml"></a>

```
[ConfigurationType](#cfn-kinesisanalyticsv2-application-monitoringconfiguration-configurationtype): String
[MetricsLevel](#cfn-kinesisanalyticsv2-application-monitoringconfiguration-metricslevel): String
[LogLevel](#cfn-kinesisanalyticsv2-application-monitoringconfiguration-loglevel): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-monitoringconfiguration-properties"></a>

`ConfigurationType`  <a name="cfn-kinesisanalyticsv2-application-monitoringconfiguration-configurationtype"></a>
Describes whether to use the default CloudWatch logging configuration for an application\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MetricsLevel`  <a name="cfn-kinesisanalyticsv2-application-monitoringconfiguration-metricslevel"></a>
Describes the granularity of the CloudWatch Logs for an application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LogLevel`  <a name="cfn-kinesisanalyticsv2-application-monitoringconfiguration-loglevel"></a>
Describes the verbosity of the CloudWatch Logs for an application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 