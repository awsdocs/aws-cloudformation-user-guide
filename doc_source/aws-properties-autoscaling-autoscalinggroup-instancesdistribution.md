# Amazon EC2 Auto Scaling AutoScalingGroup InstancesDistribution<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution"></a>

<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-description"></a>The `InstancesDistribution` property type describes an instances distribution for an Auto Scaling group with [MixedInstancesPolicy](aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.md)\. The instances distribution specifies the distribution of On\-Demand Instances and Spot Instances, the maximum price to pay for Spot Instances, and how the Auto Scaling group allocates instance types\.

<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-inheritance"></a> `InstancesDistribution` is a property of the [MixedInstancesPolicy](aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.md) property type\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-syntax.json"></a>

```
{
  "[OnDemandAllocationStrategy](#cfn-as-mixedinstancespolicy-ondemandallocationstrategy)" : String,
  "[OnDemandBaseCapacity](#cfn-as-mixedinstancespolicy-ondemandbasecapacity)" : Integer,
  "[OnDemandPercentageAboveBaseCapacity](#cfn-as-mixedinstancespolicy-ondemandpercentageabovebasecapacity)" : Integer,
  "[SpotAllocationStrategy](#cfn-as-mixedinstancespolicy-spotallocationstrategy)" : String,
  "[SpotInstancePools](#cfn-as-mixedinstancespolicy-spotinstancepools)" : Integer,
  "[SpotMaxPrice](#cfn-as-mixedinstancespolicy-spotmaxprice)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-syntax.yaml"></a>

```
[OnDemandAllocationStrategy](#cfn-as-mixedinstancespolicy-ondemandallocationstrategy): String
[OnDemandBaseCapacity](#cfn-as-mixedinstancespolicy-ondemandbasecapacity): Integer
[OnDemandPercentageAboveBaseCapacity](#cfn-as-mixedinstancespolicy-ondemandpercentageabovebasecapacity): Integer
[SpotAllocationStrategy](#cfn-as-mixedinstancespolicy-spotallocationstrategy): String
[SpotInstancePools](#cfn-as-mixedinstancespolicy-spotinstancepools): Integer
[SpotMaxPrice](#cfn-as-mixedinstancespolicy-spotmaxprice): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-properties"></a>

`OnDemandAllocationStrategy`  <a name="cfn-as-mixedinstancespolicy-ondemandallocationstrategy"></a>
Indicates how to allocate instance types to fulfill On\-Demand capacity\.  
The only valid value is `prioritized`, which is also the default value\. This strategy uses the order of instance types in the `Overrides` array of [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md) to define the launch priority of each instance type\. The first instance type in the array is prioritized higher than the last\. If all your On\-Demand capacity cannot be fulfilled using your highest priority instance, then the Auto Scaling groups launches the remaining capacity using the second priority instance type, and so on\.  
*Required*: No  
*Type*: String  
*Pattern*: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OnDemandBaseCapacity`  <a name="cfn-as-mixedinstancespolicy-ondemandbasecapacity"></a>
The minimum amount of the Auto Scaling group's capacity that must be fulfilled by On\-Demand Instances\. This base portion is provisioned first as your group scales\.  
The default value is `0`\. If you leave this parameter set to `0`, On\-Demand Instances are launched as a percentage of the Auto Scaling group's desired capacity, per the `OnDemandPercentageAboveBaseCapacity` setting\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OnDemandPercentageAboveBaseCapacity`  <a name="cfn-as-mixedinstancespolicy-ondemandpercentageabovebasecapacity"></a>
Controls the percentages of On\-Demand Instances and Spot Instances for your additional capacity beyond `OnDemandBaseCapacity`\.  
The range is 0–100\. The default value is `100`\. If you leave this parameter set to `100`, the percentages are 100% for On\-Demand Instances and 0% for Spot Instances\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SpotAllocationStrategy`  <a name="cfn-as-mixedinstancespolicy-spotallocationstrategy"></a>
Indicates how to allocate Spot capacity across Spot pools\.   
The only valid value is `lowest-price`, which is also the default value\. The Auto Scaling group selects the cheapest Spot pools and evenly allocates your Spot capacity across the number of Spot pools that you specify\.  
*Required*: No  
*Type*: String  
*Pattern*: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SpotInstancePools`  <a name="cfn-as-mixedinstancespolicy-spotinstancepools"></a>
The number of Spot pools to use to allocate your Spot capacity\. The Spot pools are determined from the different instance types in the `Overrides` array of [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md)\.  
The range is 1–20 and the default is `2`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SpotMaxPrice`  <a name="cfn-as-mixedinstancespolicy-spotmaxprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\. If you leave this value blank \(which is the default\), the maximum Spot price is set at the On\-Demand price\. Minimum length of 1\. Maximum length of 255\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution-seealso"></a>
+ [InstancesDistribution](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_InstancesDistribution.html) in the *Amazon EC2 Auto Scaling API Reference*