# Amazon Kinesis Data Analytics Application ParallelismConfiguration<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-description"></a>The `ParallelismConfiguration` property type specifies parameters for how a Java\-based Amazon Kinesis Data Analytics application executes multiple tasks simultaneously\.

<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-inheritance"></a> `ParallelismConfiguration` is a property of the [FlinkApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration.md) resource\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-syntax.json"></a>

```
{
  "[ConfigurationType](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-configurationtype)" : String,
  "[ParallelismPerKPU](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelismperkpu)" : Integer,
  "[AutoScalingEnabled](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-autoscalingenabled)" : Boolean,
  "[Parallelism](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelism)" : Integer
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-syntax.yaml"></a>

```
[ConfigurationType](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-configurationtype): String
[ParallelismPerKPU](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelismperkpu): Integer
[AutoScalingEnabled](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-autoscalingenabled): Boolean
[Parallelism](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelism): Integer
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-properties"></a>

`ConfigurationType`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-configurationtype"></a>
Describes whether the application uses the default parallelism for the Kinesis Data Analytics service\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ParallelismPerKPU`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelismperkpu"></a>
Describes the number of parallel tasks that a Java\-based Kinesis Data Analytics application can perform per Kinesis Processing Unit \(KPU\) used by the application\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AutoScalingEnabled`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-autoscalingenabled"></a>
Describes whether the Kinesis Data Analytics service can increase the parallelism of the application in response to increased throughput\.   
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Parallelism`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelism"></a>
Describes the initial number of parallel tasks that a Java\-based Kinesis Data Analytics application can perform\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 