# AWS::ECS::CapacityProvider ManagedScaling<a name="aws-properties-ecs-capacityprovider-managedscaling"></a>

The `ManagedScaling` property specifies the settings for the Auto Scaling group capacity provider\.

When managed scaling is enabled, Amazon ECS manages the scale\-in and scale\-out actions of the Auto Scaling group\. Amazon ECS manages a target tracking scaling policy using an Amazon ECS\-managed CloudWatch metric with the specified `targetCapacity` value as the target value for the metric\. For more information, see [Using Managed Scaling](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/asg-capacity-providers.html#asg-capacity-providers-managed-scaling) in the *Amazon Elastic Container Service Developer Guide*\.

If managed scaling is disabled, the user must manage the scaling of the Auto Scaling group\.

## Syntax<a name="aws-properties-ecs-capacityprovider-managedscaling-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-capacityprovider-managedscaling-syntax.json"></a>

```
{
  "[MaximumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-maximumscalingstepsize)" : Integer,
  "[MinimumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-minimumscalingstepsize)" : Integer,
  "[Status](#cfn-ecs-capacityprovider-managedscaling-status)" : String,
  "[TargetCapacity](#cfn-ecs-capacityprovider-managedscaling-targetcapacity)" : Integer
}
```

### YAML<a name="aws-properties-ecs-capacityprovider-managedscaling-syntax.yaml"></a>

```
  [MaximumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-maximumscalingstepsize): Integer
  [MinimumScalingStepSize](#cfn-ecs-capacityprovider-managedscaling-minimumscalingstepsize): Integer
  [Status](#cfn-ecs-capacityprovider-managedscaling-status): String
  [TargetCapacity](#cfn-ecs-capacityprovider-managedscaling-targetcapacity): Integer
```

## Properties<a name="aws-properties-ecs-capacityprovider-managedscaling-properties"></a>

`MaximumScalingStepSize`  <a name="cfn-ecs-capacityprovider-managedscaling-maximumscalingstepsize"></a>
The maximum number of container instances that Amazon ECS will scale in or scale out at one time\. If this parameter is omitted, the default value of `10000` is used\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinimumScalingStepSize`  <a name="cfn-ecs-capacityprovider-managedscaling-minimumscalingstepsize"></a>
The minimum number of container instances that Amazon ECS will scale in or scale out at one time\. If this parameter is omitted, the default value of `1` is used\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-ecs-capacityprovider-managedscaling-status"></a>
Whether or not to enable managed scaling for the capacity provider\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetCapacity`  <a name="cfn-ecs-capacityprovider-managedscaling-targetcapacity"></a>
The target capacity value for the capacity provider\. The specified value must be greater than `0` and less than or equal to `100`\. A value of `100` will result in the Amazon EC2 instances in your Auto Scaling group being completely utilized\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)