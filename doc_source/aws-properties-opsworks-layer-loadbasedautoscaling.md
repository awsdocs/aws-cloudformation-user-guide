# AWS::OpsWorks::Layer LoadBasedAutoScaling<a name="aws-properties-opsworks-layer-loadbasedautoscaling"></a>

Describes a layer's load\-based auto scaling configuration\.

## Syntax<a name="aws-properties-opsworks-layer-loadbasedautoscaling-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-layer-loadbasedautoscaling-syntax.json"></a>

```
{
  "[DownScaling](#cfn-opsworks-layer-loadbasedautoscaling-downscaling)" : AutoScalingThresholds,
  "[Enable](#cfn-opsworks-layer-loadbasedautoscaling-enable)" : Boolean,
  "[UpScaling](#cfn-opsworks-layer-loadbasedautoscaling-upscaling)" : AutoScalingThresholds
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

## Properties<a name="aws-properties-opsworks-layer-loadbasedautoscaling-properties"></a>

`DownScaling`  <a name="cfn-opsworks-layer-loadbasedautoscaling-downscaling"></a>
An `AutoScalingThresholds` object that describes the downscaling configuration, which defines how and when AWS OpsWorks Stacks reduces the number of instances\.  
*Required*: No  
*Type*: [AutoScalingThresholds](aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enable`  <a name="cfn-opsworks-layer-loadbasedautoscaling-enable"></a>
Whether load\-based auto scaling is enabled for the layer\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpScaling`  <a name="cfn-opsworks-layer-loadbasedautoscaling-upscaling"></a>
An `AutoScalingThresholds` object that describes the upscaling configuration, which defines how and when AWS OpsWorks Stacks increases the number of instances\.  
*Required*: No  
*Type*: [AutoScalingThresholds](aws-properties-opsworks-layer-loadbasedautoscaling-autoscalingthresholds.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)