# AWS::AutoScaling::AutoScalingGroup InstancesDistribution<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution"></a>

 `InstancesDistribution` is a subproperty of [MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html) that describes an instances distribution for an Auto Scaling group\. The instances distribution specifies the distribution of On\-Demand Instances and Spot Instances, the maximum price to pay for Spot Instances, and how the Auto Scaling group allocates instance types to fulfill On\-Demand and Spot capacities\. 

For more information and example configurations, see [Auto Scaling groups with multiple instance types and purchase options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-purchase-options.html) in the *Amazon EC2 Auto Scaling User Guide*\.

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
Indicates how to allocate instance types to fulfill On\-Demand capacity\. The only valid value is `prioritized`, which is also the default value\. This strategy uses the order of instance types in the `LaunchTemplateOverrides` to define the launch priority of each instance type\. The first instance type in the array is prioritized higher than the last\. If all your On\-Demand capacity cannot be fulfilled using your highest priority instance, then the Auto Scaling group launches the remaining capacity using the second priority instance type, and so on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnDemandBaseCapacity`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandbasecapacity"></a>
The minimum amount of the Auto Scaling group's capacity that must be fulfilled by On\-Demand Instances\. This base portion is provisioned first as your group scales\. Defaults to 0 if not specified\. If you specify weights for the instance types in the overrides, set the value of `OnDemandBaseCapacity` in terms of the number of capacity units, and not the number of instances\.  
An update to this setting means a gradual replacement of instances to adjust the current On\-Demand Instance levels\. When replacing instances, Amazon EC2 Auto Scaling launches new instances before terminating the old ones\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`OnDemandPercentageAboveBaseCapacity`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandpercentageabovebasecapacity"></a>
Controls the percentages of On\-Demand Instances and Spot Instances for your additional capacity beyond `OnDemandBaseCapacity`\. Expressed as a number \(for example, 20 specifies 20% On\-Demand Instances, 80% Spot Instances\)\. Defaults to 100 if not specified\. If set to 100, only On\-Demand Instances are provisioned\.  
An update to this setting means a gradual replacement of instances to adjust the current On\-Demand and Spot Instance levels for your additional capacity above the base capacity\. When replacing instances, Amazon EC2 Auto Scaling launches new instances before terminating the old ones\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SpotAllocationStrategy`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotallocationstrategy"></a>
If the allocation strategy is `lowest-price`, the Auto Scaling group launches instances using the Spot pools with the lowest price, and evenly allocates your instances across the number of Spot pools that you specify\. Defaults to `lowest-price` if not specified\.  
If the allocation strategy is `capacity-optimized` \(recommended\), the Auto Scaling group launches instances using Spot pools that are optimally chosen based on the available Spot capacity\. Alternatively, you can use `capacity-optimized-prioritized` and set the order of instance types in the list of launch template overrides from highest to lowest priority \(from first to last in the list\)\. Amazon EC2 Auto Scaling honors the instance type priorities on a best\-effort basis but optimizes for capacity first\.   
Valid values: `lowest-price` \| `capacity-optimized` \| `capacity-optimized-prioritized`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotInstancePools`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotinstancepools"></a>
The number of Spot Instance pools to use to allocate your Spot capacity\. The Spot pools are determined from the different instance types in the overrides\. Valid only when the Spot allocation strategy is `lowest-price`\. Value must be in the range of 1 to 20\. Defaults to 2 if not specified\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotMaxPrice`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotmaxprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\. If you leave the value at its default \(empty\), Amazon EC2 Auto Scaling uses the On\-Demand price as the maximum Spot price\. To remove a value that you previously set, include the property but specify an empty string \(""\) for the value\.   
If your maximum price is lower than the Spot price for the instance types that you selected, your Spot Instances are not launched\.
Valid Range: Minimum value of 0\.001  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)