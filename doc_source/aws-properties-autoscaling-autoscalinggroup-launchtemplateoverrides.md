# AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides"></a>

 `LaunchTemplateOverrides` is a subproperty of [LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html) that describes an override for a launch template\. Currently, the only supported override is instance type\.

The maximum number of instance type overrides that can be associated with an Auto Scaling group is 20\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.json"></a>

```
{
  "[InstanceType](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype)" : String,
  "[WeightedCapacity](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-weightedcapacity)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.yaml"></a>

```
  [InstanceType](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype): String
  [WeightedCapacity](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-weightedcapacity): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-properties"></a>

`InstanceType`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype"></a>
The instance type\. You must use an instance type that is supported in your requested Region and Availability Zones\. For more information, see [Available Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableInstanceTypes) in the *Amazon EC2 User Guide for Linux Instances\.*   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeightedCapacity`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-weightedcapacity"></a>
The number of capacity units, which gives the instance type a proportional weight to other instance types\. For example, larger instance types are generally weighted more than smaller instance types\. These are the same units that you chose to set the desired capacity in terms of instances, or a performance attribute such as vCPUs, memory, or I/O\.  
For more information, see [Instance Weighting for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-instance-weighting.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
Valid Range: Minimum value of 1\. Maximum value of 999\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)