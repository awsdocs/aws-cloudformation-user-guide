# Amazon EC2 Auto Scaling ScalingPolicy TargetTrackingConfiguration<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration"></a>

The `TargetTrackingConfiguration` property configures a target tracking scaling policy\. `TargetTrackingConfiguration` is a property of the [AWS::AutoScaling::ScalingPolicy](aws-properties-as-policy.md) resource\. For more information, see [PutScalingPolicy](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutScalingPolicy.html) in the *Amazon EC2 Auto Scaling API Reference*\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-syntax.json"></a>

```
{
  "[CustomizedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-customizedmetricspecification)" : [*CustomizedMetricSpecification*](aws-properties-autoscaling-scalingpolicy-customizedmetricspecification.md),
  "[DisableScaleIn](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-disablescalein)" : Boolean,
  "[PredefinedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-predefinedmetricspecification)" : [*PredefinedMetricSpecification*](aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification.md),
  "[TargetValue](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-syntax.yaml"></a>

```
[CustomizedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-customizedmetricspecification):
  [*CustomizedMetricSpecification*](aws-properties-autoscaling-scalingpolicy-customizedmetricspecification.md)
[DisableScaleIn](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-disablescalein): Boolean
[PredefinedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-predefinedmetricspecification):
  [*PredefinedMetricSpecification*](aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification.md)
[TargetValue](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-properties"></a>

For more information about each property, including constraints and valid values, see [TargetTrackingConfiguration](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_ScalingPolicy.html) in the *Amazon EC2 Auto Scaling API Reference*\.

`CustomizedMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-customizedmetricspecification"></a>
A customized metric\.  
*Required*: No  
*Type*: [Amazon EC2 Auto Scaling ScalingPolicy CustomizedMetricSpecification](aws-properties-autoscaling-scalingpolicy-customizedmetricspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DisableScaleIn`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-disablescalein"></a>
Indicates whether to disable scale\-in for the target tracking policy\. If `true`, the target tracking policy will not scale in the Auto Scaling group\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PredefinedMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-predefinedmetricspecification"></a>
A predefined metric\.  
*Required*: No  
*Type*: [Amazon EC2 Auto Scaling ScalingPolicy PredefinedMetricSpecification](aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetValue`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-targetvalue"></a>
The target value for the metric\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)