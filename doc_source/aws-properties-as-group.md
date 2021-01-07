# AWS::AutoScaling::AutoScalingGroup<a name="aws-properties-as-group"></a>

The AWS::AutoScaling::AutoScalingGroup resource defines an Amazon EC2 Auto Scaling group, which is a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management\.

**Note**  
Amazon EC2 Auto Scaling configures instances launched as part of an Auto Scaling group using either a launch template or a launch configuration\. We recommend that you use a launch template to make sure that you can use the latest features of Amazon EC2, such as Dedicated Hosts and T2 Unlimited instances\. For more information, see [Creating a launch template for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html)\. You can find sample launch templates in [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)\.

For more information, see [CreateAutoScalingGroup](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CreateAutoScalingGroup.html) and [UpdateAutoScalingGroup](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_UpdateAutoScalingGroup.html) in the *Amazon EC2 Auto Scaling API Reference*\. For more information about Amazon EC2 Auto Scaling, see the [Amazon EC2 Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)\. 

## Syntax<a name="aws-properties-as-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-group-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::AutoScalingGroup",
  "Properties" : {
      "[AutoScalingGroupName](#cfn-autoscaling-autoscalinggroup-autoscalinggroupname)" : String,
      "[AvailabilityZones](#cfn-as-group-availabilityzones)" : [ String, ... ],
      "[CapacityRebalance](#cfn-as-group-capacityrebalance)" : Boolean,
      "[Cooldown](#cfn-as-group-cooldown)" : String,
      "[DesiredCapacity](#cfn-as-group-desiredcapacity)" : String,
      "[HealthCheckGracePeriod](#cfn-as-group-healthcheckgraceperiod)" : Integer,
      "[HealthCheckType](#cfn-as-group-healthchecktype)" : String,
      "[InstanceId](#cfn-as-group-instanceid)" : String,
      "[LaunchConfigurationName](#cfn-as-group-launchconfigurationname)" : String,
      "[LaunchTemplate](#cfn-as-group-launchtemplate)" : LaunchTemplateSpecification,
      "[LifecycleHookSpecificationList](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist)" : [ LifecycleHookSpecification, ... ],
      "[LoadBalancerNames](#cfn-as-group-loadbalancernames)" : [ String, ... ],
      "[MaxInstanceLifetime](#cfn-as-group-maxinstancelifetime)" : Integer,
      "[MaxSize](#cfn-as-group-maxsize)" : String,
      "[MetricsCollection](#cfn-as-group-metricscollection)" : [ MetricsCollection, ... ],
      "[MinSize](#cfn-as-group-minsize)" : String,
      "[MixedInstancesPolicy](#cfn-as-group-mixedinstancespolicy)" : MixedInstancesPolicy,
      "[NewInstancesProtectedFromScaleIn](#cfn-as-group-newinstancesprotectedfromscalein)" : Boolean,
      "[NotificationConfigurations](#cfn-as-group-notificationconfigurations)" : [ NotificationConfiguration, ... ],
      "[PlacementGroup](#cfn-as-group-placementgroup)" : String,
      "[ServiceLinkedRoleARN](#cfn-autoscaling-autoscalinggroup-servicelinkedrolearn)" : String,
      "[Tags](#cfn-as-group-tags)" : [ TagProperty, ... ],
      "[TargetGroupARNs](#cfn-as-group-targetgrouparns)" : [ String, ... ],
      "[TerminationPolicies](#cfn-as-group-termpolicy)" : [ String, ... ],
      "[VPCZoneIdentifier](#cfn-as-group-vpczoneidentifier)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-properties-as-group-syntax.yaml"></a>

```
Type: AWS::AutoScaling::AutoScalingGroup
Properties: 
  [AutoScalingGroupName](#cfn-autoscaling-autoscalinggroup-autoscalinggroupname): String
  [AvailabilityZones](#cfn-as-group-availabilityzones): 
    - String
  [CapacityRebalance](#cfn-as-group-capacityrebalance): Boolean
  [Cooldown](#cfn-as-group-cooldown): String
  [DesiredCapacity](#cfn-as-group-desiredcapacity): String
  [HealthCheckGracePeriod](#cfn-as-group-healthcheckgraceperiod): Integer
  [HealthCheckType](#cfn-as-group-healthchecktype): String
  [InstanceId](#cfn-as-group-instanceid): String
  [LaunchConfigurationName](#cfn-as-group-launchconfigurationname): String
  [LaunchTemplate](#cfn-as-group-launchtemplate): 
    LaunchTemplateSpecification
  [LifecycleHookSpecificationList](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist): 
    - LifecycleHookSpecification
  [LoadBalancerNames](#cfn-as-group-loadbalancernames): 
    - String
  [MaxInstanceLifetime](#cfn-as-group-maxinstancelifetime): Integer
  [MaxSize](#cfn-as-group-maxsize): String
  [MetricsCollection](#cfn-as-group-metricscollection): 
    - MetricsCollection
  [MinSize](#cfn-as-group-minsize): String
  [MixedInstancesPolicy](#cfn-as-group-mixedinstancespolicy): 
    MixedInstancesPolicy
  [NewInstancesProtectedFromScaleIn](#cfn-as-group-newinstancesprotectedfromscalein): Boolean
  [NotificationConfigurations](#cfn-as-group-notificationconfigurations): 
    - NotificationConfiguration
  [PlacementGroup](#cfn-as-group-placementgroup): String
  [ServiceLinkedRoleARN](#cfn-autoscaling-autoscalinggroup-servicelinkedrolearn): String
  [Tags](#cfn-as-group-tags): 
    - TagProperty
  [TargetGroupARNs](#cfn-as-group-targetgrouparns): 
    - String
  [TerminationPolicies](#cfn-as-group-termpolicy): 
    - String
  [VPCZoneIdentifier](#cfn-as-group-vpczoneidentifier): 
    - String
```

## Properties<a name="aws-properties-as-group-properties"></a>

`AutoScalingGroupName`  <a name="cfn-autoscaling-autoscalinggroup-autoscalinggroupname"></a>
The name of the Auto Scaling group\. This name must be unique per Region per account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AvailabilityZones`  <a name="cfn-as-group-availabilityzones"></a>
A list of Availability Zones where instances in the Auto Scaling group can be created\. You must specify one of the following properties: `VPCZoneIdentifier` or `AvailabilityZones`\. If your account supports EC2\-Classic and VPC, this property is required to create an Auto Scaling group that launches instances into EC2\-Classic\.   
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityRebalance`  <a name="cfn-as-group-capacityrebalance"></a>
Indicates whether Capacity Rebalancing is enabled\. For more information, see [Amazon EC2 Auto Scaling Capacity Rebalancing](https://docs.aws.amazon.com/autoscaling/ec2/userguide/capacity-rebalance.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cooldown`  <a name="cfn-as-group-cooldown"></a>
The amount of time, in seconds, after a scaling activity completes before another scaling activity can start\. The default value is `300`\. This setting applies when using simple scaling policies, but not when using other scaling policies or scheduled scaling\. For more information, see [Scaling cooldowns for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/Cooldown.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredCapacity`  <a name="cfn-as-group-desiredcapacity"></a>
The desired capacity is the initial capacity of the Auto Scaling group at the time of its creation and the capacity it attempts to maintain\. It can scale beyond this capacity if you configure automatic scaling\.  
The number must be greater than or equal to the minimum size of the group and less than or equal to the maximum size of the group\. If you do not specify a desired capacity when creating the stack, the default is the minimum size of the group\.  
CloudFormation marks the Auto Scaling group as successful \(by setting its status to CREATE\_COMPLETE\) when the desired capacity is reached\. However, if `SpotPrice` is set in the [launch configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html), then desired capacity is not used as a criteria for success, because whether your request is fulfilled depends on Spot Instance capacity and your maximum price\. If the current Spot price is less than your specified maximum price, Amazon EC2 Auto Scaling uses `DesiredCapacity` as the target capacity for the group\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckGracePeriod`  <a name="cfn-as-group-healthcheckgraceperiod"></a>
The amount of time, in seconds, that Amazon EC2 Auto Scaling waits before checking the health status of an EC2 instance that has come into service\. The default value is `0`\. For more information, see [Health checks for Auto Scaling instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
If you are adding an `ELB` health check, you must specify this property\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckType`  <a name="cfn-as-group-healthchecktype"></a>
The service to use for the health checks\. The valid values are `EC2` \(default\) and `ELB`\. If you configure an Auto Scaling group to use load balancer \(ELB\) health checks, it considers the instance unhealthy if it fails either the EC2 status checks or the load balancer health checks\. For more information, see [Health checks for Auto Scaling instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-as-group-instanceid"></a>
The ID of the instance used to base the launch configuration on\. If specified, Amazon EC2 Auto Scaling uses the configuration values from the specified instance to create a new launch configuration\. For more information, see [Creating an Auto Scaling group using an EC2 instance](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-asg-from-instance.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
To get the instance ID, use the EC2 [DescribeInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeInstances.html) API operation\.  
If you specify `LaunchTemplate`, `MixedInstancesPolicy`, or `LaunchConfigurationName`, don't specify `InstanceId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchConfigurationName`  <a name="cfn-as-group-launchconfigurationname"></a>
The name of the [launch configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) to use to launch instances\.  
If you specify `LaunchTemplate`, `MixedInstancesPolicy`, or `InstanceId`, don't specify `LaunchConfigurationName`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-as-group-launchtemplate"></a>
Properties used to specify the [launch template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) and version to use to launch instances\. You can alternatively associate a launch template to the Auto Scaling group by specifying a `MixedInstancesPolicy`\.  
If you omit this property, you must specify `MixedInstancesPolicy`, `LaunchConfigurationName`, or `InstanceId`\.  
*Required*: Conditional  
*Type*: [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleHookSpecificationList`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist"></a>
One or more lifecycle hooks for the group, which specify actions to perform when Amazon EC2 Auto Scaling launches or terminates instances\.  
*Required*: No  
*Type*: List of [LifecycleHookSpecification](aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerNames`  <a name="cfn-as-group-loadbalancernames"></a>
A list of Classic Load Balancers associated with this Auto Scaling group\. For Application Load Balancers, Network Load Balancers, and Gateway Load Balancers, specify the `TargetGroupARNs` property instead\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxInstanceLifetime`  <a name="cfn-as-group-maxinstancelifetime"></a>
The maximum amount of time, in seconds, that an instance can be in service\. The default is null\. If specified, the value must be either 0 or a number equal to or greater than 86,400 seconds \(1 day\)\. For more information, see [Replacing Auto Scaling instances based on maximum instance lifetime](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-max-instance-lifetime.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-as-group-maxsize"></a>
The maximum size of the group\.  
With a mixed instances policy that uses instance weighting, Amazon EC2 Auto Scaling may need to go above `MaxSize` to meet your capacity requirements\. In this event, Amazon EC2 Auto Scaling will never go above `MaxSize` by more than your largest instance weight \(weights that define how many units each instance contributes to the desired capacity of the group\)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricsCollection`  <a name="cfn-as-group-metricscollection"></a>
Enables the monitoring of group metrics of an Auto Scaling group\. By default, these metrics are disabled\.   
*Required*: No  
*Type*: [List](aws-properties-as-metricscollection.md) of [MetricsCollection](aws-properties-as-metricscollection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-as-group-minsize"></a>
The minimum size of the group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MixedInstancesPolicy`  <a name="cfn-as-group-mixedinstancespolicy"></a>
An embedded object that specifies a mixed instances policy\.  
The policy includes properties that not only define the distribution of On\-Demand Instances and Spot Instances, the maximum price to pay for Spot Instances \(optional\), and how the Auto Scaling group allocates instance types to fulfill On\-Demand and Spot capacities, but also the properties that specify the instance configuration information—the launch template and instance types\. The policy can also include a weight for each instance type and different launch templates for individual instance types\.  
For more information, see [Auto Scaling groups with multiple instance types and purchase options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-purchase-options.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
If you specify `LaunchTemplate`, `InstanceId`, or `LaunchConfigurationName`, don't specify `MixedInstancesPolicy`\.  
*Required*: Conditional  
*Type*: [MixedInstancesPolicy](aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NewInstancesProtectedFromScaleIn`  <a name="cfn-as-group-newinstancesprotectedfromscalein"></a>
Indicates whether newly launched instances are protected from termination by Amazon EC2 Auto Scaling when scaling in\. For more information about preventing instances from terminating on scale in, see [Instance Protection](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html#instance-protection) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationConfigurations`  <a name="cfn-as-group-notificationconfigurations"></a>
Configures an Auto Scaling group to send notifications when specified events take place\.  
*Required*: No  
*Type*: List of [NotificationConfiguration](aws-properties-as-notificationconfigurations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementGroup`  <a name="cfn-as-group-placementgroup"></a>
The name of the placement group into which you want to launch your instances\. A placement group is a logical grouping of instances within a single Availability Zone\. For more information, see [Placement Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceLinkedRoleARN`  <a name="cfn-autoscaling-autoscalinggroup-servicelinkedrolearn"></a>
The Amazon Resource Name \(ARN\) of the service\-linked role that the Auto Scaling group uses to call other AWS services on your behalf\. By default, Amazon EC2 Auto Scaling uses a service\-linked role named AWSServiceRoleForAutoScaling, which it creates if it does not exist\. For more information, see [Service\-linked roles for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-service-linked-role.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-as-group-tags"></a>
One or more tags\. You can tag your Auto Scaling group and propagate the tags to the Amazon EC2 instances it launches\. For more information, see [Tagging Auto Scaling groups and instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-tagging.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: List of [TagProperty](aws-properties-as-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupARNs`  <a name="cfn-as-group-targetgrouparns"></a>
One or more Amazon Resource Names \(ARN\) of load balancer target groups to associate with the Auto Scaling group\. Instances are registered as targets in a target group, and traffic is routed to the target group\. For more information, see [Elastic Load Balancing and Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-load-balancer.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminationPolicies`  <a name="cfn-as-group-termpolicy"></a>
A policy or a list of policies that are used to select the instances to terminate\. The policies are executed in the order that you list them\. The termination policies supported by Amazon EC2 Auto Scaling: `OldestInstance`, `OldestLaunchConfiguration`, `NewestInstance`, `ClosestToNextInstanceHour`, `Default`, `OldestLaunchTemplate`, and `AllocationStrategy`\. For more information, see [Controlling which Auto Scaling instances terminate during scale in](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCZoneIdentifier`  <a name="cfn-as-group-vpczoneidentifier"></a>
A list of subnet IDs for a virtual private cloud \(VPC\) where instances in the Auto Scaling group can be created\. If you specify `VPCZoneIdentifier` with `AvailabilityZones`, the subnets that you specify for this property must reside in those Availability Zones\.   
If this resource specifies public subnets and is also in a VPC that is defined in the same stack template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the [VPC\-gateway attachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-gateway-attachment.html)\.  
When you update `VPCZoneIdentifier`, this retains the same Auto Scaling group and replaces old instances with new ones, according to the specified subnets\. You can optionally specify how AWS CloudFormation handles these updates by using an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

## Return values<a name="aws-properties-as-group-return-values"></a>

### Ref<a name="aws-properties-as-group-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-myasgroup-NT5EUXTNTXXD`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Remarks<a name="aws-properties-as-group--remarks"></a>

When you update the launch template or launch configuration for an Auto Scaling group, this update action does not deploy any change across the running Amazon EC2 instances in the Auto Scaling group\. All new instances will get the updated configuration, but existing instances continue to run with the configuration that they were originally launched with\. This works the same way as any other Auto Scaling group\. 

You can add an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) to your stack to perform rolling updates \(or replace the group\) when a change has been made to the group\. You can find sample update policies for rolling updates in [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\. Alternatively, you can force a rolling update on your instances at any time after updating the stack by starting an instance refresh\. For more information, see [Replacing Auto Scaling instances based on an instance refresh](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-instance-refresh.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Examples<a name="aws-properties-as-group--examples"></a>

The following examples create or make changes to an Auto Scaling group\. 

For more template snippets, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

### Single instance Auto Scaling group with a parameters section<a name="aws-properties-as-group--examples--Single_instance_Auto_Scaling_group_with_a_parameters_section"></a>

The following example creates an Auto Scaling group with a single instance and an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource that controls the configuration of any instances that are launched by the Auto Scaling group\.

It references [parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) for the `VPCZoneIdentifier` and `Version` \(`LaunchTemplate`\) properties\. Each of these parameters is a variable that you can specify when you create or update the stack\.

CloudFormation supports parameters from the AWS Systems Manager Parameter Store\. In this example, the `ImageId` property of the AWS::EC2::LaunchTemplate references the latest Amazon Linux 2 AMI from the Parameter Store\. For more information, see [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) in the *AWS Systems Manager User Guide* and the blog post [Query for the latest Amazon Linux AMI IDs using AWS Systems Manager Parameter Store](http://aws.amazon.com/blogs/compute/query-for-the-latest-amazon-linux-ami-ids-using-aws-systems-manager-parameter-store/) on the AWS Compute Blog\.

#### JSON<a name="aws-properties-as-group--examples--Single_instance_Auto_Scaling_group_with_a_parameters_section--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "LatestAmiId": {
      "Description": "Region specific image from the Parameter Store",
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
    },
    "myLaunchTemplateVersionNumber":{
      "Type":"String"
    },
    "Subnets":{
      "Type":"CommaDelimitedList"
    }
  },
  "Resources":{
    "myLaunchTemplate":{
      "Type":"AWS::EC2::LaunchTemplate",
      "Properties":{
        "LaunchTemplateData":{
          "ImageId":{
            "Ref":"LatestAmiId"
          },
          "InstanceType":"t3.micro"
        }
      }
    },
    "myASG": {
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties": {
        "MinSize":"0",
        "MaxSize":"1",
        "DesiredCapacity":"1",
        "LaunchTemplate": {
          "LaunchTemplateId": {
            "Ref":"myLaunchTemplate"
          },
          "Version":{
            "Ref":"myLaunchTemplateVersionNumber"
          }
        },
        "VPCZoneIdentifier":{
          "Ref":"Subnets"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-group--examples--Single_instance_Auto_Scaling_group_with_a_parameters_section--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Parameters:
  LatestAmiId:
    Description: Region specific image from the Parameter Store
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: '/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2'
  myLaunchTemplateVersionNumber:
    Type: String
  Subnets:
    Type: CommaDelimitedList
Resources:
  myLaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties: 
      LaunchTemplateData: 
        ImageId: !Ref LatestAmiId
        InstanceType: t3.micro
  myASG:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      MinSize: '0'
      MaxSize: '1'
      DesiredCapacity: '1'
      LaunchTemplate:
        LaunchTemplateId: !Ref myLaunchTemplate
        Version: !Ref myLaunchTemplateVersionNumber
      VPCZoneIdentifier: !Ref Subnets
```

### Auto Scaling group with CloudWatch monitoring enabled and defined tags<a name="aws-properties-as-group--examples--Auto_Scaling_group_with_CloudWatch_monitoring_enabled_and_defined_tags_"></a>

The following example creates an Auto Scaling group named `myASG` with CloudWatch monitoring \(`MetricsCollection`\) enabled and custom tags\. The first tag, `Environment`=`Production`, is assigned to the Auto Scaling group and to any EC2 instances launched as part of the Auto Scaling group\. The second tag, `Purpose`=`WebServerGroup`, is assigned only to the Auto Scaling group itself\. 

Each instance has 300 seconds to warm up before receiving its first health check\. The launch template provisions T2 instances in unlimited mode using the `CPUCredits` property\. A block device mapping specifies an EBS volume to attach to each instance, in addition to attaching the volumes specified by the AMI\. Because `Monitoring` is enabled, EC2 metric data will be available at 1\-minute intervals \(known as detailed monitoring\) through CloudWatch\. 

This example also uses intrinsic functions to assign values to certain properties dynamically\. To get the version number of the launch template, it specifies the launch template's logical name and the latest version number of the launch template in the format `myLaunchTemplate.LatestVersionNumber` with the intrinsic function [GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. It also uses the [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html) function to customize the name of the launch template to include the stack name and the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function to reference two [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html) resources for the Auto Scaling group that are declared elsewhere in the same template\. 

#### JSON<a name="aws-properties-as-group--examples--Auto_Scaling_group_with_CloudWatch_monitoring_enabled_and_defined_tags_--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources":{
    "myLaunchTemplate":{
      "Type":"AWS::EC2::LaunchTemplate",
      "Properties":{
        "LaunchTemplateName":{"Fn::Sub":"${AWS::StackName}-launch-template"},
        "LaunchTemplateData":{
          "BlockDeviceMappings":[{
            "Ebs":{
              "VolumeSize":"22",
              "VolumeType":"gp2",
              "DeleteOnTermination": true,
              "Encrypted": true
            },
            "DeviceName":"/dev/xvdcz"
          }],
          "CreditSpecification":{
            "CpuCredits":"unlimited"
          },
          "ImageId":"ami-02354e95b39ca8dec",
          "InstanceType":"t2.micro",
          "KeyName":"my-key-pair-useast1",
          "Monitoring":{"Enabled":true},
          "SecurityGroupIds":["sg-7c227019", "sg-903004f8"]
        }
      }
    },
    "myASG":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "AutoScalingGroupName":"myASG",
        "MinSize": "1",
        "MaxSize": "6",
        "DesiredCapacity": "2",
        "HealthCheckGracePeriod":300,
        "LaunchTemplate":{
          "LaunchTemplateId":{
            "Ref":"myLaunchTemplate"
          },
          "Version":{
            "Fn::GetAtt":[
              "myLaunchTemplate",
              "LatestVersionNumber"
            ]
          }
        },
        "VPCZoneIdentifier":[ { "Ref" : "myPublicSubnet1" }, { "Ref" : "myPublicSubnet2" } ],
        "MetricsCollection":[
          {
            "Granularity":"1Minute",
            "Metrics":[
              "GroupMinSize",
              "GroupMaxSize"
            ]
          }
        ],
        "Tags":[
          {
            "Key":"Environment",
            "Value":"Production",
            "PropagateAtLaunch":"true"
          },
          {
            "Key":"Purpose",
            "Value":"WebServerGroup",
            "PropagateAtLaunch":"false"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-group--examples--Auto_Scaling_group_with_CloudWatch_monitoring_enabled_and_defined_tags_--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myLaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties: 
      LaunchTemplateName: !Sub ${AWS::StackName}-launch-template
      LaunchTemplateData: 
        BlockDeviceMappings: 
          - Ebs:
              VolumeSize: 22
              VolumeType: gp2
              DeleteOnTermination: true
              Encrypted: true
            DeviceName: /dev/xvdcz
        CreditSpecification: 
          CpuCredits: Unlimited
        ImageId: ami-02354e95b39ca8dec
        InstanceType: t2.micro
        KeyName: my-key-pair-useast1
        Monitoring: 
          Enabled: true
        SecurityGroupIds: 
          - sg-7c227019
          - sg-903004f8
  myASG:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      AutoScalingGroupName: myASG
      MinSize: "1"
      MaxSize: "6"
      DesiredCapacity: "2"
      HealthCheckGracePeriod: 300
      LaunchTemplate:
        LaunchTemplateId: !Ref myLaunchTemplate
        Version: !GetAtt myLaunchTemplate.LatestVersionNumber
      VPCZoneIdentifier:
        - !Ref myPublicSubnet1
        - !Ref myPublicSubnet2
      MetricsCollection: 
        - Granularity: "1Minute"
          Metrics: 
            - "GroupMinSize"
            - "GroupMaxSize"
      Tags:
        - Key: Environment
          Value: Production
          PropagateAtLaunch: "true"
        - Key: Purpose
          Value: WebServerGroup
          PropagateAtLaunch: "false"
```

## See also<a name="aws-properties-as-group--seealso"></a>
+ [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)
+ [AWS CloudFormation stack updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)
+ [Suspending and resuming scaling processes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-suspend-resume-processes.html) in the *Amazon EC2 Auto Scaling User Guide*

