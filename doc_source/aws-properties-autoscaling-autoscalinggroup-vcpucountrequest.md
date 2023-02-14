# AWS::AutoScaling::AutoScalingGroup VCpuCountRequest<a name="aws-properties-autoscaling-autoscalinggroup-vcpucountrequest"></a>

`VCpuCountRequest` is a property of the `InstanceRequirements` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property type that describes the minimum and maximum number of vCPUs for an instance type\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-vcpucountrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-vcpucountrequest-syntax.json"></a>

```
{
  "[Max](#cfn-autoscaling-autoscalinggroup-vcpucountrequest-max)" : Integer,
  "[Min](#cfn-autoscaling-autoscalinggroup-vcpucountrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-vcpucountrequest-syntax.yaml"></a>

```
  [Max](#cfn-autoscaling-autoscalinggroup-vcpucountrequest-max): Integer
  [Min](#cfn-autoscaling-autoscalinggroup-vcpucountrequest-min): Integer
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-vcpucountrequest-properties"></a>

`Max`  <a name="cfn-autoscaling-autoscalinggroup-vcpucountrequest-max"></a>
The maximum number of vCPUs\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-autoscaling-autoscalinggroup-vcpucountrequest-min"></a>
The minimum number of vCPUs\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)