# AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy<a name="aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy"></a>

Use this structure to launch multiple instance types and On\-Demand Instances and Spot Instances within a single Auto Scaling group\.

A mixed instances policy contains information that Amazon EC2 Auto Scaling can use to launch instances and help optimize your costs\. For more information, see [Auto Scaling groups with multiple instance types and purchase options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups.html) in the *Amazon EC2 Auto Scaling User Guide*\.

You can create a mixed instances policy for new and existing Auto Scaling groups\. You must use a launch template to configure the policy\. You cannot use a launch configuration\.

There are key differences between Spot Instances and On\-Demand Instances:
+ The price for Spot Instances varies based on demand
+ Amazon EC2 can terminate an individual Spot Instance as the availability of, or price for, Spot Instances changes

When a Spot Instance is terminated, Amazon EC2 Auto Scaling group attempts to launch a replacement instance to maintain the desired capacity for the group\. 

 `MixedInstancesPolicy` is a property of the [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource\.

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
The instances distribution\.  
*Required*: No  
*Type*: [InstancesDistribution](aws-properties-autoscaling-autoscalinggroup-instancesdistribution.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-as-mixedinstancespolicy-launchtemplate"></a>
One or more launch templates and the instance types \(overrides\) that are used to launch EC2 instances to fulfill On\-Demand and Spot capacities\.  
*Required*: Yes  
*Type*: [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)