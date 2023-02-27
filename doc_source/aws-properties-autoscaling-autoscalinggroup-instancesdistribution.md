# AWS::AutoScaling::AutoScalingGroup InstancesDistribution<a name="aws-properties-autoscaling-autoscalinggroup-instancesdistribution"></a>

Use this structure to specify the distribution of On\-Demand Instances and Spot Instances and the allocation strategies used to fulfill On\-Demand and Spot capacities for a mixed instances policy\.

For more information, see [Auto Scaling groups with multiple instance types and purchase options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups.html) in the *Amazon EC2 Auto Scaling User Guide*\.

 `InstancesDistribution` is a property of the [AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html) property type\. 

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
The allocation strategy to apply to your On\-Demand Instances when they are launched\. Possible instance types are determined by the launch template overrides that you specify\.  
The following lists the valid values:    
lowest\-price  
Uses price to determine which instance types are the highest priority, launching the lowest priced instance types within an Availability Zone first\. This is the default value for Auto Scaling groups that specify `InstanceRequirements`\.   
prioritized  
You set the order of instance types for the launch template overrides from highest to lowest priority \(from first to last in the list\)\. Amazon EC2 Auto Scaling launches your highest priority instance types first\. If all your On\-Demand capacity cannot be fulfilled using your highest priority instance type, then Amazon EC2 Auto Scaling launches the remaining capacity using the second priority instance type, and so on\. This is the default value for Auto Scaling groups that don't specify `InstanceRequirements` and cannot be used for groups that do\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnDemandBaseCapacity`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandbasecapacity"></a>
The minimum amount of the Auto Scaling group's capacity that must be fulfilled by On\-Demand Instances\. This base portion is launched first as your group scales\.  
This number has the same unit of measurement as the group's desired capacity\. If you change the default unit of measurement \(number of instances\) by specifying weighted capacity values in your launch template overrides list, or by changing the default desired capacity type setting of the group, you must specify this number using the same unit of measurement\.  
Default: 0  
An update to this setting means a gradual replacement of instances to adjust the current On\-Demand Instance levels\. When replacing instances, Amazon EC2 Auto Scaling launches new instances before terminating the previous ones\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`OnDemandPercentageAboveBaseCapacity`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-ondemandpercentageabovebasecapacity"></a>
Controls the percentages of On\-Demand Instances and Spot Instances for your additional capacity beyond `OnDemandBaseCapacity`\. Expressed as a number \(for example, 20 specifies 20% On\-Demand Instances, 80% Spot Instances\)\. If set to 100, only On\-Demand Instances are used\.  
Default: 100  
An update to this setting means a gradual replacement of instances to adjust the current On\-Demand and Spot Instance levels for your additional capacity higher than the base capacity\. When replacing instances, Amazon EC2 Auto Scaling launches new instances before terminating the previous ones\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SpotAllocationStrategy`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotallocationstrategy"></a>
The allocation strategy to apply to your Spot Instances when they are launched\. Possible instance types are determined by the launch template overrides that you specify\.  
The following lists the valid values:    
capacity\-optimized  
Requests Spot Instances using pools that are optimally chosen based on the available Spot capacity\. This strategy has the lowest risk of interruption\. To give certain instance types a higher chance of launching first, use `capacity-optimized-prioritized`\.  
capacity\-optimized\-prioritized  
You set the order of instance types for the launch template overrides from highest to lowest priority \(from first to last in the list\)\. Amazon EC2 Auto Scaling honors the instance type priorities on a best effort basis but optimizes for capacity first\. Note that if the On\-Demand allocation strategy is set to `prioritized`, the same priority is applied when fulfilling On\-Demand capacity\. This is not a valid value for Auto Scaling groups that specify `InstanceRequirements`\.  
lowest\-price  
Requests Spot Instances using the lowest priced pools within an Availability Zone, across the number of Spot pools that you specify for the `SpotInstancePools` property\. To ensure that your desired capacity is met, you might receive Spot Instances from several pools\. This is the default value, but it might lead to high interruption rates because this strategy only considers instance price and not available capacity\.  
price\-capacity\-optimized \(recommended\)  
The price and capacity optimized allocation strategy looks at both price and capacity to select the Spot Instance pools that are the least likely to be interrupted and have the lowest possible price\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotInstancePools`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotinstancepools"></a>
The number of Spot Instance pools across which to allocate your Spot Instances\. The Spot pools are determined from the different instance types in the overrides\. Valid only when the `SpotAllocationStrategy` is `lowest-price`\. Value must be in the range of 1–20\.  
Default: 2  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotMaxPrice`  <a name="cfn-autoscaling-autoscalinggroup-instancesdistribution-spotmaxprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\. If your maximum price is lower than the Spot price for the instance types that you selected, your Spot Instances are not launched\. We do not recommend specifying a maximum price because it can lead to increased interruptions\. When Spot Instances launch, you pay the current Spot price\. To remove a maximum price that you previously set, include the property but specify an empty string \(""\) for the value\.  
If you specify a maximum price, your instances will be interrupted more frequently than if you do not specify one\.
Valid Range: Minimum value of 0\.001  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)