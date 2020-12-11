# AWS::KinesisAnalyticsV2::Application FlinkApplicationConfiguration<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration"></a>

Describes configuration parameters for a Flink\-based Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-syntax.json"></a>

```
{
  "[CheckpointConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-checkpointconfiguration)" : CheckpointConfiguration,
  "[MonitoringConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-monitoringconfiguration)" : MonitoringConfiguration,
  "[ParallelismConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-parallelismconfiguration)" : ParallelismConfiguration
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-syntax.yaml"></a>

```
  [CheckpointConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-checkpointconfiguration): 
    CheckpointConfiguration
  [MonitoringConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-monitoringconfiguration): 
    MonitoringConfiguration
  [ParallelismConfiguration](#cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-parallelismconfiguration): 
    ParallelismConfiguration
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration-properties"></a>

`CheckpointConfiguration`  <a name="cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-checkpointconfiguration"></a>
Describes an application's checkpointing configuration\. Checkpointing is the process of persisting application state for fault tolerance\. For more information, see [ Checkpoints for Fault Tolerance](https://ci.apache.org/projects/flink/flink-docs-release-1.8/concepts/programming-model.html#checkpoints-for-fault-tolerance) in the [Apache Flink Documentation](https://ci.apache.org/projects/flink/flink-docs-release-1.8/)\.   
*Required*: No  
*Type*: [CheckpointConfiguration](aws-properties-kinesisanalyticsv2-application-checkpointconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringConfiguration`  <a name="cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-monitoringconfiguration"></a>
Describes configuration parameters for Amazon CloudWatch logging for an application\.  
*Required*: No  
*Type*: [MonitoringConfiguration](aws-properties-kinesisanalyticsv2-application-monitoringconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParallelismConfiguration`  <a name="cfn-kinesisanalyticsv2-application-flinkapplicationconfiguration-parallelismconfiguration"></a>
Describes parameters for how an application executes multiple tasks simultaneously\.  
*Required*: No  
*Type*: [ParallelismConfiguration](aws-properties-kinesisanalyticsv2-application-parallelismconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration--seealso"></a>
+  [FlinkApplicationConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_FlinkApplicationConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 

