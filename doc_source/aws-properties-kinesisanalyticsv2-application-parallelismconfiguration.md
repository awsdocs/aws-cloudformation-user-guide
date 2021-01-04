# AWS::KinesisAnalyticsV2::Application ParallelismConfiguration<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration"></a>

Describes parameters for how a Flink\-based Kinesis Data Analytics application executes multiple tasks simultaneously\. For more information about parallelism, see [Parallel Execution](https://ci.apache.org/projects/flink/flink-docs-release-1.8/dev/parallel.html) in the [Apache Flink Documentation](https://ci.apache.org/projects/flink/flink-docs-release-1.8/)\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-syntax.json"></a>

```
{
  "[AutoScalingEnabled](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-autoscalingenabled)" : Boolean,
  "[ConfigurationType](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-configurationtype)" : String,
  "[Parallelism](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelism)" : Integer,
  "[ParallelismPerKPU](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelismperkpu)" : Integer
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-syntax.yaml"></a>

```
  [AutoScalingEnabled](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-autoscalingenabled): Boolean
  [ConfigurationType](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-configurationtype): String
  [Parallelism](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelism): Integer
  [ParallelismPerKPU](#cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelismperkpu): Integer
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration-properties"></a>

`AutoScalingEnabled`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-autoscalingenabled"></a>
Describes whether the Kinesis Data Analytics service can increase the parallelism of the application in response to increased throughput\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigurationType`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-configurationtype"></a>
Describes whether the application uses the default parallelism for the Kinesis Data Analytics service\. You must set this property to `CUSTOM` in order to change your application's `AutoScalingEnabled`, `Parallelism`, or `ParallelismPerKPU` properties\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CUSTOM | DEFAULT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parallelism`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelism"></a>
Describes the initial number of parallel tasks that a Java\-based Kinesis Data Analytics application can perform\. The Kinesis Data Analytics service can increase this number automatically if [ParallelismConfiguration:AutoScalingEnabled](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_ParallelismConfiguration.html#kinesisanalytics-Type-ParallelismConfiguration-AutoScalingEnabled.html) is set to `true`\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParallelismPerKPU`  <a name="cfn-kinesisanalyticsv2-application-parallelismconfiguration-parallelismperkpu"></a>
Describes the number of parallel tasks that a Java\-based Kinesis Data Analytics application can perform per Kinesis Processing Unit \(KPU\) used by the application\. For more information about KPUs, see [Amazon Kinesis Data Analytics Pricing](https://aws.amazon.com/kinesis/data-analytics/pricing/)\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-parallelismconfiguration--seealso"></a>
+  [ParallelismConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_ParallelismConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 

