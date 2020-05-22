# AWS::OpsWorks::Layer AutoScalingThresholds<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds"></a>

Describes a load\-based auto scaling upscaling or downscaling threshold configuration, which specifies when AWS OpsWorks Stacks starts or stops load\-based instances\.

## Syntax<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-syntax.json"></a>

```
{
  "[CpuThreshold](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-cputhreshold)" : Double,
  "[IgnoreMetricsTime](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-ignoremetricstime)" : Integer,
  "[InstanceCount](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-instancecount)" : Integer,
  "[LoadThreshold](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-loadthreshold)" : Double,
  "[MemoryThreshold](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-memorythreshold)" : Double,
  "[ThresholdsWaitTime](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-thresholdwaittime)" : Integer
}
```

### YAML<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-syntax.yaml"></a>

```
  [CpuThreshold](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-cputhreshold): Double
  [IgnoreMetricsTime](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-ignoremetricstime): Integer
  [InstanceCount](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-instancecount): Integer
  [LoadThreshold](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-loadthreshold): Double
  [MemoryThreshold](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-memorythreshold): Double
  [ThresholdsWaitTime](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-thresholdwaittime): Integer
```

## Properties<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-properties"></a>

`CpuThreshold`  <a name="cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-cputhreshold"></a>
The CPU utilization threshold, as a percent of the available CPU\. A value of \-1 disables the threshold\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IgnoreMetricsTime`  <a name="cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-ignoremetricstime"></a>
The amount of time \(in minutes\) after a scaling event occurs that AWS OpsWorks Stacks should ignore metrics and suppress additional scaling events\. For example, AWS OpsWorks Stacks adds new instances following an upscaling event but the instances won't start reducing the load until they have been booted and configured\. There is no point in raising additional scaling events during that operation, which typically takes several minutes\. `IgnoreMetricsTime` allows you to direct AWS OpsWorks Stacks to suppress scaling events long enough to get the new instances online\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceCount`  <a name="cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-instancecount"></a>
The number of instances to add or remove when the load exceeds a threshold\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadThreshold`  <a name="cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-loadthreshold"></a>
The load threshold\. A value of \-1 disables the threshold\. For more information about how load is computed, see [Load \(computing\)](http://en.wikipedia.org/wiki/Load_%28computing%29)\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemoryThreshold`  <a name="cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-memorythreshold"></a>
The memory utilization threshold, as a percent of the available memory\. A value of \-1 disables the threshold\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThresholdsWaitTime`  <a name="cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-thresholdwaittime"></a>
The amount of time, in minutes, that the load must exceed a threshold before more instances are added or removed\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)