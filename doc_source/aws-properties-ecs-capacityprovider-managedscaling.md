# AWS::ECS::CapacityProvider ManagedScaling<a name="aws-properties-ecs-capacityprovider-managedscaling"></a>

The managed scaling settings for the Auto Scaling group capacity provider\.

When managed scaling is enabled, Amazon ECS manages the scale\-in and scale\-out actions of the Auto Scaling group\. Amazon ECS manages a target tracking scaling policy using an Amazon ECS managed CloudWatch metric with the specified `targetCapacity` value as the target value for the metric\. For more information, see [Using managed scaling](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/asg-capacity-providers.html#asg-capacity-providers-managed-scaling) in the *Amazon Elastic Container Service Developer Guide*\.

If managed scaling is off, the user must manage the scaling of the Auto Scaling group\.

## Syntax<a name="aws-properties-ecs-capacityprovider-managedscaling-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-capacityprovider-managedscaling-syntax.json"></a>

```
{
  "[InstanceWarmupPeriod](#cfn-ecs-capacityprovider-managedscaling-instancewarmupperiod)" : Integer,
  "[MaximumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-maximumscalingstepsize)" : Integer,
  "[MinimumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-minimumscalingstepsize)" : Integer,
  "[Status](#cfn-ecs-capacityprovider-managedscaling-status)" : String,
  "[TargetCapacity](#cfn-ecs-capacityprovider-managedscaling-targetcapacity)" : Integer
}
```

### YAML<a name="aws-properties-ecs-capacityprovider-managedscaling-syntax.yaml"></a>

```
  [InstanceWarmupPeriod](#cfn-ecs-capacityprovider-managedscaling-instancewarmupperiod): Integer
  [MaximumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-maximumscalingstepsize): Integer
  [MinimumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-minimumscalingstepsize): Integer
  [Status](#cfn-ecs-capacityprovider-managedscaling-status): String
  [TargetCapacity](#cfn-ecs-capacityprovider-managedscaling-targetcapacity): Integer
```

## Properties<a name="aws-properties-ecs-capacityprovider-managedscaling-properties"></a>

`InstanceWarmupPeriod`  <a name="cfn-ecs-capacityprovider-managedscaling-instancewarmupperiod"></a>
The period of time, in seconds, after a newly launched Amazon EC2 instance can contribute to CloudWatch metrics for Auto Scaling group\. If this parameter is omitted, the default value of `300` seconds is used\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumScalingStepSize`  <a name="cfn-ecs-capacityprovider-managedscaling-maximumscalingstepsize"></a>
The maximum number of Amazon EC2 instances that Amazon ECS will scale out at one time\. The scale in process is not affected by this parameter\. If this parameter is omitted, the default value of `1` is used\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumScalingStepSize`  <a name="cfn-ecs-capacityprovider-managedscaling-minimumscalingstepsize"></a>
The minimum number of Amazon EC2 instances that Amazon ECS will scale out at one time\. The scale in process is not affected by this parameter If this parameter is omitted, the default value of `1` is used\.  
When additional capacity is required, Amazon ECS will scale up the minimum scaling step size even if the actual demand is less than the minimum scaling step size\.  
If you use a capacity provider with an Auto Scaling group configured with more than one Amazon EC2 instance type or Availability Zone, Amazon ECS will scale up by the exact minimum scaling step size value and will ignore both the maximum scaling step size as well as the capacity demand\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-ecs-capacityprovider-managedscaling-status"></a>
Determines whether to use managed scaling for the capacity provider\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetCapacity`  <a name="cfn-ecs-capacityprovider-managedscaling-targetcapacity"></a>
The target capacity value for the capacity provider\. The specified value must be greater than `0` and less than or equal to `100`\. A value of `100` results in the Amazon EC2 instances in your Auto Scaling group being completely used\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)