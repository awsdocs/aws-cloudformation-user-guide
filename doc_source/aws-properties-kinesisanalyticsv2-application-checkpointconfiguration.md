# Amazon Kinesis Data Analytics Application CheckpointConfiguration<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-description"></a>The `CheckpointConfiguration` property type specifies an application's checkpointing configuration\. Checkpointing is the process of persisting application state for fault tolerance\.

<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-inheritance"></a> `CheckpointConfiguration` is a property of the [AWS::KinesisAnalyticsV2::Application](aws-resource-kinesisanalyticsv2-application.md) resource\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-syntax.json"></a>

```
{
  "[ConfigurationType](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-configurationtype)" : String,
  "[CheckpointInterval](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointinterval)" : Integer,
  "[MinPauseBetweenCheckpoints](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-minpausebetweencheckpoints)" : Integer,
  "[CheckpointingEnabled](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointingenabled)" : Boolean
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-syntax.yaml"></a>

```
[ConfigurationType](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-configurationtype): String
[CheckpointInterval](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointinterval): Integer
[MinPauseBetweenCheckpoints](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-minpausebetweencheckpoints): Integer
[CheckpointingEnabled](#cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointingenabled): Boolean
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-checkpointconfiguration-properties"></a>

`ConfigurationType`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-configurationtype"></a>
Describes whether the application uses Amazon Kinesis Data Analytics' default checkpointing behavior\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CheckpointInterval`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointinterval"></a>
Describes the interval in milliseconds between checkpoint operations\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MinPauseBetweenCheckpoints`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-minpausebetweencheckpoints"></a>
Describes the minimum time in milliseconds after a checkpoint operation completes that a new checkpoint operation can start\. If a checkpoint operation takes longer than the CheckpointInterval, the application otherwise performs continual checkpoint operations\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CheckpointingEnabled`  <a name="cfn-kinesisanalyticsv2-application-checkpointconfiguration-checkpointingenabled"></a>
Describes whether checkpointing is enabled for a Java\-based Kinesis Data Analytics application\.   
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 