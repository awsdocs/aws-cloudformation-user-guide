# AWS::AutoScaling::ScalingPolicy TargetTrackingConfiguration<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration"></a>

 `TargetTrackingConfiguration` is a subproperty of [ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html) that specifies a target tracking scaling policy to use with Amazon EC2 Auto Scaling\. 

For more information, see [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutScalingPolicy.html) in the *Amazon EC2 Auto Scaling API Reference*\. For more information about scaling policies, see [Dynamic scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scale-based-on-demand.html) in the *Amazon EC2 Auto Scaling User Guide*\. 

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-syntax.json"></a>

```
{
  "[CustomizedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-customizedmetricspecification)" : CustomizedMetricSpecification,
  "[DisableScaleIn](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-disablescalein)" : Boolean,
  "[PredefinedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-predefinedmetricspecification)" : PredefinedMetricSpecification,
  "[TargetValue](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-syntax.yaml"></a>

```
  [CustomizedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-customizedmetricspecification): 
    CustomizedMetricSpecification
  [DisableScaleIn](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-disablescalein): Boolean
  [PredefinedMetricSpecification](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-predefinedmetricspecification): 
    PredefinedMetricSpecification
  [TargetValue](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration-properties"></a>

`CustomizedMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-customizedmetricspecification"></a>
A customized metric\. You must specify either a predefined metric or a customized metric\.  
*Required*: Conditional  
*Type*: [CustomizedMetricSpecification](aws-properties-autoscaling-scalingpolicy-customizedmetricspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableScaleIn`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-disablescalein"></a>
Indicates whether scaling in by the target tracking scaling policy is disabled\. If scaling in is disabled, the target tracking scaling policy doesn't remove instances from the Auto Scaling group\. Otherwise, the target tracking scaling policy can remove instances from the Auto Scaling group\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-predefinedmetricspecification"></a>
A predefined metric\. You must specify either a predefined metric or a customized metric\.  
*Required*: Conditional  
*Type*: [PredefinedMetricSpecification](aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration-targetvalue"></a>
The target value for the metric\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)