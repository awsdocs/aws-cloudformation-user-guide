# AWS OpsWorks LoadBasedAutoScaling Type<a name="aws-properties-opsworks-layer-loadbasedautoscaling"></a>

Describes the load\-based automatic scaling configuration for an [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md) resource type\. For more information, see [SetLoadBasedAutoScaling](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_SetLoadBasedAutoScaling.html) in the *AWS OpsWorks Stacks API Reference*\.

## Syntax<a name="w3ab2c21c14e1569b5"></a>

### JSON<a name="aws-properties-opsworks-layer-loadbasedautoscaling-syntax.json"></a>

```
{
  "[DownScaling](#cfn-opsworks-layer-loadbasedautoscaling-downscaling)" : { AutoScalingThresholds },
  "[Enable](#cfn-opsworks-layer-loadbasedautoscaling-enable)" : Boolean,
  "[UpScaling](#cfn-opsworks-layer-loadbasedautoscaling-upscaling)" : { AutoScalingThresholds }
}
```

### YAML<a name="aws-properties-opsworks-layer-loadbasedautoscaling-syntax.yaml"></a>

```
[DownScaling](#cfn-opsworks-layer-loadbasedautoscaling-downscaling):
  AutoScalingThresholds
[Enable](#cfn-opsworks-layer-loadbasedautoscaling-enable): Boolean
[UpScaling](#cfn-opsworks-layer-loadbasedautoscaling-upscaling):
  AutoScalingThresholds
```

## Properties<a name="w3ab2c21c14e1569b7"></a>

`DownScaling`  <a name="cfn-opsworks-layer-loadbasedautoscaling-downscaling"></a>
The threshold below which the instances are scaled down \(stopped\)\. If the load falls below this threshold for a specified amount of time, AWS OpsWorks stops a specified number of instances\.  
*Required*: No  
*Type*: [AWS OpsWorks AutoScalingThresholds Type](aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds.md)

`Enable`  <a name="cfn-opsworks-layer-loadbasedautoscaling-enable"></a>
Whether to enable automatic load\-based scaling for the layer\.  
*Required*: No  
*Type*: Boolean

`UpScaling`  <a name="cfn-opsworks-layer-loadbasedautoscaling-upscaling"></a>
The threshold above which the instances are scaled up \(added\)\. If the load exceeds this thresholds for a specified amount of time, AWS OpsWorks starts a specified number of instances\.  
*Required*: No  
*Type*: [AWS OpsWorks AutoScalingThresholds Type](aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds.md)