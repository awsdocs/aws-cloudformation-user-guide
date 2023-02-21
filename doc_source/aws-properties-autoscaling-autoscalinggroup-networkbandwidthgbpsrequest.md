# AWS::AutoScaling::AutoScalingGroup NetworkBandwidthGbpsRequest<a name="aws-properties-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest"></a>

`NetworkBandwidthGbpsRequest` is a property of the `InstanceRequirements` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property type that describes the minimum and maximum network bandwidth for an instance type, in Gbps\.

**Note**  
Setting the minimum bandwidth does not guarantee that your instance will achieve the minimum bandwidth\. Amazon EC2 will identify instance types that support the specified minimum bandwidth, but the actual bandwidth of your instance might go below the specified minimum at times\. For more information, see [Available instance bandwidth](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-network-bandwidth.html#available-instance-bandwidth) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-syntax.json"></a>

```
{
  "[Max](#cfn-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-max)" : Integer,
  "[Min](#cfn-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-syntax.yaml"></a>

```
  [Max](#cfn-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-max): Integer
  [Min](#cfn-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-min): Integer
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-properties"></a>

`Max`  <a name="cfn-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-max"></a>
The maximum amount of network bandwidth, in gigabits per second \(Gbps\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-autoscaling-autoscalinggroup-networkbandwidthgbpsrequest-min"></a>
The minimum amount of network bandwidth, in gigabits per second \(Gbps\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)