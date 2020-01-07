# AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy"></a>

 `MixedInstancesPolicy` is a property of [AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) that describes a mixed instances policy for an Amazon EC2 Auto Scaling group\. With mixed instances, your Auto Scaling group can provision a combination of On\-Demand Instances and Spot Instances across multiple instance types\. For more information, see [Auto Scaling Groups with Multiple Instance Types and Purchase Options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-purchase-options.html) in the *Amazon EC2 Auto Scaling User Guide*\.

You can create a mixed instances policy for a new Auto Scaling group, or you can create it for an existing group by updating the group to specify `MixedInstancesPolicy` as the top\-level parameter instead of a launch configuration or template\. If you specify a `MixedInstancesPolicy`, you must specify a launch template as a property of the policy\. You cannot specify a launch configuration for the policy\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-syntax.json"></a>

```
{
  "[InstancesDistribution](#cfn-as-mixedinstancespolicy-instancesdistribution)" : [InstancesDistribution](aws-properties-autoscaling-autoscalinggroup-instancesdistribution.md),
  "[LaunchTemplate](#cfn-as-mixedinstancespolicy-launchtemplate)" : [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md)
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-syntax.yaml"></a>

```
  [InstancesDistribution](#cfn-as-mixedinstancespolicy-instancesdistribution): 
    [InstancesDistribution](aws-properties-autoscaling-autoscalinggroup-instancesdistribution.md)
  [LaunchTemplate](#cfn-as-mixedinstancespolicy-launchtemplate): 
    [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md)
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-properties"></a>

`InstancesDistribution`  <a name="cfn-as-mixedinstancespolicy-instancesdistribution"></a>
The instances distribution to use\.  
If you leave this property unspecified, the value for each property in `InstancesDistribution` uses a default value\.  
*Required*: No  
*Type*: [InstancesDistribution](aws-properties-autoscaling-autoscalinggroup-instancesdistribution.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-as-mixedinstancespolicy-launchtemplate"></a>
The launch template and instance types \(overrides\)\.  
*Required*: Yes  
*Type*: [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)