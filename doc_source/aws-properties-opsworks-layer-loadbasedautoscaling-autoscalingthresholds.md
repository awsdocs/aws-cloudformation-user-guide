# AWS OpsWorks AutoScalingThresholds Type<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds"></a>

Describes the scaling thresholds for the [AWS OpsWorks LoadBasedAutoScaling Type](aws-properties-opsworks-layer-loadbasedautoscaling.md) property\. For more information, see [AutoScalingThresholds](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_AutoScalingThresholds.html) in the *AWS OpsWorks Stacks API Reference*\.

## Syntax<a name="w3ab2c21c14e1347b5"></a>

### JSON<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-cputhreshold)" : Number,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-ignoremetricstime)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-instancecount)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-loadthreshold)" : Number,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-memorythreshold)" : Number,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-thresholdwaittime)" : Integer
}
```

### YAML<a name="aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-cputhreshold): Number
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-ignoremetricstime): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-instancecount): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-loadthreshold): Number
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-memorythreshold): Number
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-autoscalingthresholds-thresholdwaittime): Integer
```

## Properties<a name="w3ab2c21c14e1347b7"></a>

`CpuThreshold`  
The percentage of CPU utilization that triggers the starting or stopping of instances \(scaling\)\.  
*Required: *No  
*Type*: Number

`IgnoreMetricsTime`  
The amount of time \(in minutes\) after a scaling event occurs that AWS OpsWorks should ignore metrics and not start any additional scaling events\.  
*Required: *No  
*Type*: Integer

`InstanceCount`  
The number of instances to add or remove when the load exceeds a threshold\.  
*Required: *No  
*Type*: Integer

`LoadThreshold`  
The degree of system load that triggers the starting or stopping of instances \(scaling\)\. For more information about how load is computed, see [Load \(computing\)](http://en.wikipedia.org/wiki/Load_%28computing%29)\.  
*Required: *No  
*Type*: Number

`MemoryThreshold`  
The percentage of memory consumption that triggers the starting or stopping of instances \(scaling\)\.  
*Required: *No  
*Type*: Number

`ThresholdsWaitTime`  
The amount of time, in minutes, that the load must exceed a threshold before instances are added or removed\.  
*Required: *No  
*Type*: Integer