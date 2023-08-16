# AWS::KinesisAnalyticsV2::Application RunConfiguration<a name="aws-properties-kinesisanalyticsv2-application-runconfiguration"></a>

Describes the starting parameters for an Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-runconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-runconfiguration-syntax.json"></a>

```
{
  "[ApplicationRestoreConfiguration](#cfn-kinesisanalyticsv2-application-runconfiguration-applicationrestoreconfiguration)" : ApplicationRestoreConfiguration,
  "[FlinkRunConfiguration](#cfn-kinesisanalyticsv2-application-runconfiguration-flinkrunconfiguration)" : FlinkRunConfiguration
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-runconfiguration-syntax.yaml"></a>

```
  [ApplicationRestoreConfiguration](#cfn-kinesisanalyticsv2-application-runconfiguration-applicationrestoreconfiguration): 
    ApplicationRestoreConfiguration
  [FlinkRunConfiguration](#cfn-kinesisanalyticsv2-application-runconfiguration-flinkrunconfiguration): 
    FlinkRunConfiguration
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-runconfiguration-properties"></a>

`ApplicationRestoreConfiguration`  <a name="cfn-kinesisanalyticsv2-application-runconfiguration-applicationrestoreconfiguration"></a>
Describes the restore behavior of a restarting application\.  
*Required*: No  
*Type*: [ApplicationRestoreConfiguration](aws-properties-kinesisanalyticsv2-application-applicationrestoreconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlinkRunConfiguration`  <a name="cfn-kinesisanalyticsv2-application-runconfiguration-flinkrunconfiguration"></a>
Describes the starting parameters for a Flink\-based Kinesis Data Analytics application\.  
*Required*: No  
*Type*: [FlinkRunConfiguration](aws-properties-kinesisanalyticsv2-application-flinkrunconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)