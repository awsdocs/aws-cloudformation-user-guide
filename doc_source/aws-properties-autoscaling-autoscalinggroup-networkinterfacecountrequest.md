# AWS::AutoScaling::AutoScalingGroup NetworkInterfaceCountRequest<a name="aws-properties-autoscaling-autoscalinggroup-networkinterfacecountrequest"></a>

`NetworkInterfaceCountRequest` is a property of the `InstanceRequirements` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property type that describes the minimum and maximum number of network interfaces for an instance type\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-networkinterfacecountrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-networkinterfacecountrequest-syntax.json"></a>

```
{
  "[Max](#cfn-autoscaling-autoscalinggroup-networkinterfacecountrequest-max)" : Integer,
  "[Min](#cfn-autoscaling-autoscalinggroup-networkinterfacecountrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-networkinterfacecountrequest-syntax.yaml"></a>

```
  [Max](#cfn-autoscaling-autoscalinggroup-networkinterfacecountrequest-max): Integer
  [Min](#cfn-autoscaling-autoscalinggroup-networkinterfacecountrequest-min): Integer
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-networkinterfacecountrequest-properties"></a>

`Max`  <a name="cfn-autoscaling-autoscalinggroup-networkinterfacecountrequest-max"></a>
The maximum number of network interfaces\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-autoscaling-autoscalinggroup-networkinterfacecountrequest-min"></a>
The minimum number of network interfaces\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)