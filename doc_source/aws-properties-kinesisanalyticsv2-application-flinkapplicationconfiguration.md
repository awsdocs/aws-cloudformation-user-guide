# Amazon Kinesis Data Analytics Application FlinkApplicationConfiguration<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-description"></a>The `FlinkApplicationConfiguration` property type describes configuration parameters for a Java\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-inheritance"></a> `FlinkApplicationConfiguration` is a property of the [ApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-syntax.json"></a>

```
{
  "[CheckpointConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-checkpointconfiguration)" : [*CheckpointConfiguration*](aws-properties-kinesisanalyticsv2-application-checkpointconfiguration.md),
  "[ParallelismConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-parallelismconfiguration)" : [*ParallelismConfiguration*](aws-properties-kinesisanalyticsv2-application-parallelismconfiguration.md),
  "[MonitoringConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-monitoringconfiguration)" : [*MonitoringConfiguration*](aws-properties-kinesisanalyticsv2-application-monitoringconfiguration.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-syntax.yaml"></a>

```
[CheckpointConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-checkpointconfiguration): [*CheckpointConfiguration*](aws-properties-kinesisanalyticsv2-application-checkpointconfiguration.md)
[ParallelismConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-parallelismconfiguration): [*ParallelismConfiguration*](aws-properties-kinesisanalyticsv2-application-parallelismconfiguration.md)
[MonitoringConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-monitoringconfiguration): [*MonitoringConfiguration*](aws-properties-kinesisanalyticsv2-application-monitoringconfiguration.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-properties"></a>

`CheckpointConfiguration`  <a name="cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-checkpointconfiguration"></a>
Describes an application's checkpointing configuration\. Checkpointing is the process of persisting application state for fault tolerance\.   
 *Required*: No  
 *Type*: [CheckpointConfiguration](aws-properties-kinesisanalyticsv2-application-checkpointconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ParallelismConfiguration`  <a name="cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-parallelismconfiguration"></a>
Describes parameters for how an application executes multiple tasks simultaneously\.  
 *Required*: No  
 *Type*: [ParallelismConfiguration](aws-properties-kinesisanalyticsv2-application-parallelismconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MonitoringConfiguration`  <a name="cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-monitoringconfiguration"></a>
Describes configuration parameters for Amazon CloudWatch logging for an application\.   
 *Required*: No  
 *Type*: [MonitoringConfiguration](aws-properties-kinesisanalyticsv2-application-monitoringconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 