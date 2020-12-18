# AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy"></a>

 `MixedInstancesPolicy` is a property of [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)\. It allows you to configure a group that diversifies across On\-Demand Instances and Spot Instances of multiple instance types\. For more information, see [Auto Scaling groups with multiple instance types and purchase options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-purchase-options.html) in the *Amazon EC2 Auto Scaling User Guide*\.

You can create a mixed instances policy for a new Auto Scaling group, or you can create it for an existing group by updating the group to specify `MixedInstancesPolicy` as the top\-level parameter instead of a launch template or launch configuration\. If you specify a `MixedInstancesPolicy`, you must specify a launch template as a property of the policy\. You cannot specify a launch configuration for the policy\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-syntax.json"></a>

```
{
  "[InstancesDistribution](#cfn-as-mixedinstancespolicy-instancesdistribution)" : InstancesDistribution,
  "[LaunchTemplate](#cfn-as-mixedinstancespolicy-launchtemplate)" : LaunchTemplate
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-syntax.yaml"></a>

```
  [InstancesDistribution](#cfn-as-mixedinstancespolicy-instancesdistribution): 
    InstancesDistribution
  [LaunchTemplate](#cfn-as-mixedinstancespolicy-launchtemplate): 
    LaunchTemplate
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy-properties"></a>

`InstancesDistribution`  <a name="cfn-as-mixedinstancespolicy-instancesdistribution"></a>
The instances distribution to use\. If you leave this property unspecified, the value for each property in `InstancesDistribution` uses a default value\.  
*Required*: No  
*Type*: [InstancesDistribution](aws-properties-autoscaling-autoscalinggroup-instancesdistribution.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-as-mixedinstancespolicy-launchtemplate"></a>
Specifies the launch template to use and optionally the instance types \(overrides\) that are used to provision EC2 instances to fulfill On\-Demand and Spot capacities\.  
*Required*: Yes  
*Type*: [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)