# AWS::AutoScaling::AutoScalingGroup InstancesDistribution<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution"></a>

 `InstancesDistribution` is a subproperty of [MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html) that describes an instances distribution for an Auto Scaling group\. The instances distribution specifies the distribution of On\-Demand Instances and Spot Instances, the maximum price to pay for Spot Instances, and how the Auto Scaling group allocates instance types to fulfill On\-Demand and Spot capacity\.

For more information, see [Auto Scaling Groups with Multiple Instance Types and Purchase Options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-purchase-options.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-syntax.json"></a>

```
{
  "[OnDemandAllocationStrategy](#cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandallocationstrategy)" : String,
  "[OnDemandBaseCapacity](#cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandbasecapacity)" : Integer,
  "[OnDemandPercentageAboveBaseCapacity](#cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandpercentageabovebasecapacity)" : Integer,
  "[SpotAllocationStrategy](#cfn-autoscaling-autoscalinggroup-instancesdistribution-spotallocationstrategy)" : String,
  "[SpotInstancePools](#cfn-autoscaling-autoscalinggroup-instancesdistribution-spotinstancepools)" : Integer,
  "[SpotMaxPrice](#cfn-autoscaling-autoscalinggroup-instancesdistribution-spotmaxprice)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-syntax.yaml"></a>

```
  [OnDemandAllocationStrategy](#cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandallocationstrategy): String
  [OnDemandBaseCapacity](#cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandbasecapacity): Integer
  [OnDemandPercentageAboveBaseCapacity](#cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandpercentageabovebasecapacity): Integer
  [SpotAllocationStrategy](#cfn-autoscaling-autoscalinggroup-instancesdistribution-spotallocationstrategy): String
  [SpotInstancePools](#cfn-autoscaling-autoscalinggroup-instancesdistribution-spotinstancepools): Integer
  [SpotMaxPrice](#cfn-autoscaling-autoscalinggroup-instancesdistribution-spotmaxprice): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-properties"></a>

`OnDemandAllocationStrategy`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandallocationstrategy"></a>
Indicates how to allocate instance types to fulfill On\-Demand capacity\.
The only valid value is `prioritized`, which is also the default value\. This strategy uses the order of instance type overrides for [LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html) to define the launch priority of each instance type\. The first instance type in the array is prioritized higher than the last\. If all your On\-Demand capacity cannot be fulfilled using your highest priority instance, then the Auto Scaling groups launches the remaining capacity using the second priority instance type, and so on\.
*Required*: No
*Type*: String
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnDemandBaseCapacity`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandbasecapacity"></a>
The minimum amount of the Auto Scaling group's capacity that must be fulfilled by On\-Demand Instances\. This base portion is provisioned first as your group scales\.
The default value is `0`\. If you leave this property set to `0`, On\-Demand Instances are launched as a percentage of the Auto Scaling group's desired capacity, per the `OnDemandPercentageAboveBaseCapacity` setting\.
*Required*: No
*Type*: Integer
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnDemandPercentageAboveBaseCapacity`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandpercentageabovebasecapacity"></a>
Controls the percentages of On\-Demand Instances and Spot Instances for your additional capacity beyond `OnDemandBaseCapacity`\.
The range is 0–100\. The default value is `100`\. If you leave this property set to `100`, the percentages are 100% for On\-Demand Instances and 0% for Spot Instances\.
*Required*: No
*Type*: Integer
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotAllocationStrategy`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotallocationstrategy"></a>
Indicates how to allocate Spot capacity across Spot pools\.
The only valid value is `lowest-price`, which is also the default value\. The Auto Scaling group selects the cheapest Spot pools and evenly allocates your Spot capacity across the number of Spot pools that you specify\.
*Required*: No
*Type*: String
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotInstancePools`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotinstancepools"></a>
The number of Spot pools to use to allocate your Spot capacity\. The Spot pools are determined from the different instance types in the Overrides array of [LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html)\.
The range is 1–20 and the default is 2\.
*Required*: No
*Type*: Integer
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotMaxPrice`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotmaxprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\. If you leave the value of this property blank \(which is the default\), the maximum Spot price is set at the On\-Demand price\.
*Required*: No
*Type*: String
*Minimum*: `0`
*Maximum*: `255`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
