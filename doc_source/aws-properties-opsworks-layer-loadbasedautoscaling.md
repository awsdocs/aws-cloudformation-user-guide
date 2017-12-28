# AWS OpsWorks LoadBasedAutoScaling Type<a name="aws-properties-opsworks-layer-loadbasedautoscaling"></a>

Describes the load\-based automatic scaling configuration for an [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md) resource type\. For more information, see [SetLoadBasedAutoScaling](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_SetLoadBasedAutoScaling.html) in the *AWS OpsWorks Stacks API Reference*\.

## Syntax<a name="w3ab2c21c14e1363b5"></a>

### JSON<a name="aws-properties-opsworks-layer-loadbasedautoscaling-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-downscaling)" : { AutoScalingThresholds },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-enable)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-upscaling)" : { AutoScalingThresholds }
}
```

### YAML<a name="aws-properties-opsworks-layer-loadbasedautoscaling-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-downscaling):
  AutoScalingThresholds
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-enable): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-loadbasedautoscaling-upscaling):
  AutoScalingThresholds
```

## Properties<a name="w3ab2c21c14e1363b7"></a>

`DownScaling`  
The threshold below which the instances are scaled down \(stopped\)\. If the load falls below this threshold for a specified amount of time, AWS OpsWorks stops a specified number of instances\.  
*Required: *No  
*Type*: [AWS OpsWorks AutoScalingThresholds Type](aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds.md)

`Enable`  
Whether to enable automatic load\-based scaling for the layer\.  
*Required: *No  
*Type*: Boolean

`UpScaling`  
The threshold above which the instances are scaled up \(added\)\. If the load exceeds this thresholds for a specified amount of time, AWS OpsWorks starts a specified number of instances\.  
*Required: *No  
*Type*: [AWS OpsWorks AutoScalingThresholds Type](aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds.md)