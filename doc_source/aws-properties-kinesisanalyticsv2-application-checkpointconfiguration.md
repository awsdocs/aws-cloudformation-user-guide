# AWS::KinesisAnalyticsV2::Application CheckpointConfiguration<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration"></a>

Describes an application's checkpointing configuration\. Checkpointing is the process of persisting application state for fault tolerance\. For more information, see [ Checkpoints for Fault Tolerance](https://ci.apache.org/projects/flink/flink-docs-release-1.8/concepts/programming-model.html#checkpoints-for-fault-tolerance) in the [Apache Flink Documentation](https://ci.apache.org/projects/flink/flink-docs-release-1.8/)\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-syntax.json"></a>

```
{
  "[CheckpointingEnabled](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointingenabled)" : Boolean,
  "[CheckpointInterval](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointinterval)" : Integer,
  "[ConfigurationType](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-configurationtype)" : String,
  "[MinPauseBetweenCheckpoints](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-minpausebetweencheckpoints)" : Integer
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-syntax.yaml"></a>

```
  [CheckpointingEnabled](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointingenabled): Boolean
  [CheckpointInterval](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointinterval): Integer
  [ConfigurationType](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-configurationtype): String
  [MinPauseBetweenCheckpoints](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-minpausebetweencheckpoints): Integer
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-properties"></a>

`CheckpointingEnabled`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointingenabled"></a>
Describes whether checkpointing is enabled for a Flink\-based Kinesis Data Analytics application\.  
If `CheckpointConfiguration.ConfigurationType` is `DEFAULT`, the application will use a `CheckpointingEnabled` value of `true`, even if this value is set to another value using this API or in application code\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CheckpointInterval`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointinterval"></a>
Describes the interval in milliseconds between checkpoint operations\.   
If `CheckpointConfiguration.ConfigurationType` is `DEFAULT`, the application will use a `CheckpointInterval` vaue of 60000, even if this value is set to another value using this API or in application code\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigurationType`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-configurationtype"></a>
Describes whether the application uses Kinesis Data Analytics' default checkpointing behavior\. You must set this property to `CUSTOM` in order to set the `CheckpointingEnabled`, `CheckpointInterval`, or `MinPauseBetweenCheckpoints` parameters\.  
If this value is set to `DEFAULT`, the application will use the following values, even if they are set to other values using APIs or application code:  
+  **CheckpointingEnabled:** true
+  **CheckpointInterval:** 60000
+  **MinPauseBetweenCheckpoints:** 5000
*Required*: Yes  
*Type*: String  
*Allowed values*: `CUSTOM | DEFAULT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinPauseBetweenCheckpoints`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-minpausebetweencheckpoints"></a>
Describes the minimum time in milliseconds after a checkpoint operation completes that a new checkpoint operation can start\. If a checkpoint operation takes longer than the `CheckpointInterval`, the application otherwise performs continual checkpoint operations\. For more information, see [ Tuning Checkpointing](https://ci.apache.org/projects/flink/flink-docs-release-1.8/ops/state/large_state_tuning.html#tuning-checkpointing) in the [Apache Flink Documentation](https://ci.apache.org/projects/flink/flink-docs-release-1.8/)\.  
If `CheckpointConfiguration.ConfigurationType` is `DEFAULT`, the application will use a `MinPauseBetweenCheckpoints` value of 5000, even if this value is set using this API or in application code\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration--seealso"></a>
+  [CheckpointConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_CheckpointConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 

