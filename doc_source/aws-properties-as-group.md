# AWS::AutoScaling::AutoScalingGroup<a name="aws-properties-as-group"></a>

The `AWS::AutoScaling::AutoScalingGroup` resource defines an Amazon EC2 Auto Scaling group, which is a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management\. 

For more information about Amazon EC2 Auto Scaling, see the [Amazon EC2 Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)\. 

**Note**  
Amazon EC2 Auto Scaling configures instances launched as part of an Auto Scaling group using either a [launch template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) or a launch configuration\. We strongly recommend that you do not use launch configurations\. They do not provide full functionality for Amazon EC2 Auto Scaling or Amazon EC2\. For more information, see [Launch configurations](https://docs.aws.amazon.com/autoscaling/ec2/userguide/launch-configurations.html) in the *Amazon EC2 Auto Scaling User Guide*\.

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
      "[Context](#cfn-as-group-context)" : String,
      "[Cooldown](#cfn-as-group-cooldown)" : String,
      "[DefaultInstanceWarmup](#cfn-as-group-defaultinstancewarmup)" : Integer,
      "[DesiredCapacity](#cfn-as-group-desiredcapacity)" : String,
      "[DesiredCapacityType](#cfn-as-group-desiredcapacitytype)" : String,
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
  [Context](#cfn-as-group-context): String
  [Cooldown](#cfn-as-group-cooldown): String
  [DefaultInstanceWarmup](#cfn-as-group-defaultinstancewarmup): Integer
  [DesiredCapacity](#cfn-as-group-desiredcapacity): String
  [DesiredCapacityType](#cfn-as-group-desiredcapacitytype): String
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
The name can contain any ASCII character 33 to 126 including most punctuation characters, digits, and upper and lowercased letters\.  
You cannot use a colon \(:\) in the name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AvailabilityZones`  <a name="cfn-as-group-availabilityzones"></a>
A list of Availability Zones where instances in the Auto Scaling group can be created\. Used for launching into the default VPC subnet in each Availability Zone when not using the `VPCZoneIdentifier` property, or for attaching a network interface when an existing network interface ID is specified in a launch template\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityRebalance`  <a name="cfn-as-group-capacityrebalance"></a>
Indicates whether Capacity Rebalancing is enabled\. Otherwise, Capacity Rebalancing is disabled\. When you turn on Capacity Rebalancing, Amazon EC2 Auto Scaling attempts to launch a Spot Instance whenever Amazon EC2 notifies that a Spot Instance is at an elevated risk of interruption\. After launching a new instance, it then terminates an old instance\. For more information, see [Use Capacity Rebalancing to handle Amazon EC2 Spot Interruptions](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-capacity-rebalancing.html) in the in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Context`  <a name="cfn-as-group-context"></a>
Reserved\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cooldown`  <a name="cfn-as-group-cooldown"></a>
 *Only needed if you use simple scaling policies\.*   
The amount of time, in seconds, between one scaling activity ending and another one starting due to simple scaling policies\. For more information, see [Scaling cooldowns for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/Cooldown.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
Default: `300` seconds  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultInstanceWarmup`  <a name="cfn-as-group-defaultinstancewarmup"></a>
The amount of time, in seconds, until a new instance is considered to have finished initializing and resource consumption to become stable after it enters the `InService` state\.   
During an instance refresh, Amazon EC2 Auto Scaling waits for the warm\-up period after it replaces an instance before it moves on to replacing the next instance\. Amazon EC2 Auto Scaling also waits for the warm\-up period before aggregating the metrics for new instances with existing instances in the Amazon CloudWatch metrics that are used for scaling, resulting in more reliable usage data\. For more information, see [Set the default instance warmup for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-default-instance-warmup.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
To manage various warm\-up settings at the group level, we recommend that you set the default instance warmup, *even if it is set to 0 seconds*\. To remove a value that you previously set, include the property but specify `-1` for the value\. However, we strongly recommend keeping the default instance warmup enabled by specifying a value of `0` or other nominal value\.
Default: None   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredCapacity`  <a name="cfn-as-group-desiredcapacity"></a>
The desired capacity is the initial capacity of the Auto Scaling group at the time of its creation and the capacity it attempts to maintain\. It can scale beyond this capacity if you configure automatic scaling\.  
The number must be greater than or equal to the minimum size of the group and less than or equal to the maximum size of the group\. If you do not specify a desired capacity when creating the stack, the default is the minimum size of the group\.  
CloudFormation marks the Auto Scaling group as successful \(by setting its status to CREATE\_COMPLETE\) when the desired capacity is reached\. However, if a maximum Spot price is set in the launch template or launch configuration that you specified, then desired capacity is not used as a criteria for success\. Whether your request is fulfilled depends on Spot Instance capacity and your maximum price\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredCapacityType`  <a name="cfn-as-group-desiredcapacitytype"></a>
The unit of measurement for the value specified for desired capacity\. Amazon EC2 Auto Scaling supports `DesiredCapacityType` for attribute\-based instance type selection only\. For more information, see [Creating an Auto Scaling group using attribute\-based instance type selection](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-asg-instance-type-requirements.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
By default, Amazon EC2 Auto Scaling specifies `units`, which translates into number of instances\.  
Valid values: `units` \| `vcpu` \| `memory-mib`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckGracePeriod`  <a name="cfn-as-group-healthcheckgraceperiod"></a>
The amount of time, in seconds, that Amazon EC2 Auto Scaling waits before checking the health status of an EC2 instance that has come into service and marking it unhealthy due to a failed health check\. This is useful if your instances do not immediately pass their health checks after they enter the `InService` state\. For more information, see [Set the health check grace period for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/health-check-grace-period.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
Default: `0` seconds  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckType`  <a name="cfn-as-group-healthchecktype"></a>
Determines whether any additional health checks are performed on the instances in this group\. Amazon EC2 health checks are always on\. For more information, see [Health checks for Auto Scaling instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
The valid values are `EC2` \(default\), `ELB`, and `VPC_LATTICE`\. The `VPC_LATTICE` health check type is reserved for use with VPC Lattice, which is in preview release and is subject to change\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-as-group-instanceid"></a>
The ID of the instance used to base the launch configuration on\. For more information, see [Create an Auto Scaling group using an EC2 instance](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-asg-from-instance.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
If you specify `LaunchTemplate`, `MixedInstancesPolicy`, or `LaunchConfigurationName`, don't specify `InstanceId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchConfigurationName`  <a name="cfn-as-group-launchconfigurationname"></a>
The name of the launch configuration to use to launch instances\.  
Required only if you don't specify `LaunchTemplate`, `MixedInstancesPolicy`, or `InstanceId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-as-group-launchtemplate"></a>
Information used to specify the launch template and version to use to launch instances\. You can alternatively associate a launch template to the Auto Scaling group by specifying a `MixedInstancesPolicy`\. For more information about creating launch templates, see [Create a launch template for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
If you omit this property, you must specify `MixedInstancesPolicy`, `LaunchConfigurationName`, or `InstanceId`\.  
*Required*: No  
*Type*: [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleHookSpecificationList`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist"></a>
One or more lifecycle hooks to add to the Auto Scaling group before instances are launched\.  
*Required*: No  
*Type*: List of [LifecycleHookSpecification](aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerNames`  <a name="cfn-as-group-loadbalancernames"></a>
A list of Classic Load Balancers associated with this Auto Scaling group\. For Application Load Balancers, Network Load Balancers, and Gateway Load Balancer, specify the `TargetGroupARNs` property instead\.  
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
For more information, see [Auto Scaling groups with multiple instance types and purchase options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: [MixedInstancesPolicy](aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NewInstancesProtectedFromScaleIn`  <a name="cfn-as-group-newinstancesprotectedfromscalein"></a>
Indicates whether newly launched instances are protected from termination by Amazon EC2 Auto Scaling when scaling in\. For more information about preventing instances from terminating on scale in, see [Using instance scale\-in protection](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-instance-protection.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationConfigurations`  <a name="cfn-as-group-notificationconfigurations"></a>
Configures an Auto Scaling group to send notifications when specified events take place\.  
*Required*: No  
*Type*: List of [NotificationConfiguration](aws-properties-as-notificationconfigurations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementGroup`  <a name="cfn-as-group-placementgroup"></a>
The name of the placement group into which to launch your instances\. For more information, see [Placement groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
A *cluster* placement group is a logical grouping of instances within a single Availability Zone\. You cannot specify multiple Availability Zones and a cluster placement group\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceLinkedRoleARN`  <a name="cfn-autoscaling-autoscalinggroup-servicelinkedrolearn"></a>
The Amazon Resource Name \(ARN\) of the service\-linked role that the Auto Scaling group uses to call other AWS service on your behalf\. By default, Amazon EC2 Auto Scaling uses a service\-linked role named `AWSServiceRoleForAutoScaling`, which it creates if it does not exist\. For more information, see [Service\-linked roles](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-service-linked-role.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-as-group-tags"></a>
One or more tags\. You can tag your Auto Scaling group and propagate the tags to the Amazon EC2 instances it launches\. Tags are not propagated to Amazon EBS volumes\. To add tags to Amazon EBS volumes, specify the tags in a launch template but use caution\. If the launch template specifies an instance tag with a key that is also specified for the Auto Scaling group, Amazon EC2 Auto Scaling overrides the value of that instance tag with the value specified by the Auto Scaling group\. For more information, see [Tag Auto Scaling groups and instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-tagging.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: List of [TagProperty](aws-properties-as-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupARNs`  <a name="cfn-as-group-targetgrouparns"></a>
The Amazon Resource Names \(ARN\) of the Elastic Load Balancing target groups to associate with the Auto Scaling group\. Instances are registered as targets with the target groups\. The target groups receive incoming traffic and route requests to one or more registered targets\. For more information, see [Use Elastic Load Balancing to distribute traffic across the instances in your Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-load-balancer.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminationPolicies`  <a name="cfn-as-group-termpolicy"></a>
A policy or a list of policies that are used to select the instance to terminate\. These policies are executed in the order that you list them\. For more information, see [Work with Amazon EC2 Auto Scaling termination policies](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-termination-policies.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
Valid values: `Default` \| `AllocationStrategy` \| `ClosestToNextInstanceHour` \| `NewestInstance` \| `OldestInstance` \| `OldestLaunchConfiguration` \| `OldestLaunchTemplate` \| `arn:aws:lambda:region:account-id:function:my-function:my-alias`   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCZoneIdentifier`  <a name="cfn-as-group-vpczoneidentifier"></a>
A list of subnet IDs for a virtual private cloud \(VPC\) where instances in the Auto Scaling group can be created\.  
If this resource specifies public subnets and is also in a VPC that is defined in the same stack template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the [VPC\-gateway attachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-gateway-attachment.html)\.  
When you update `VPCZoneIdentifier`, this retains the same Auto Scaling group and replaces old instances with new ones, according to the specified subnets\. You can optionally specify how CloudFormation handles these updates by using an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.
Required to launch instances into a nondefault VPC\. If you specify `VPCZoneIdentifier` with `AvailabilityZones`, the subnets that you specify for this property must reside in those Availability Zones\.   
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

## Return values<a name="aws-properties-as-group-return-values"></a>

### Ref<a name="aws-properties-as-group-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-myasgroup-NT5EUXTNTXXD`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Remarks<a name="aws-properties-as-group--remarks"></a>

When you update the launch template or launch configuration for an Auto Scaling group, this update action does not deploy any change across the running Amazon EC2 instances in the Auto Scaling group\. All new instances will get the updated configuration, but existing instances continue to run with the configuration that they were originally launched with\. This works the same way as any other Auto Scaling group\. 

You can add an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) to your stack to perform rolling updates \(or replace the group\) when a change has been made to the group\. You can find a sample update policy for rolling updates in [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\. Alternatively, you can force a rolling update on your instances at any time after updating the stack by starting an instance refresh\. For more information, see [Replace Auto Scaling instances based on an instance refresh](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-instance-refresh.html) in the *Amazon EC2 Auto Scaling User Guide*\.

You can use a [CreationPolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-creationpolicy.html) with an Auto Scaling group to prevent its status from reaching create complete until CloudFormation receives a specified number of success signals\. For more information, see [Use a CreationPolicy to Wait for On\-Instance Configurations](http://aws.amazon.com/blogs/devops/use-a-creationpolicy-to-wait-for-on-instance-configurations/) on the AWS DevOps Blog\. For an example template, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

Note that Amazon EC2 Auto Scaling provides scaling activities to help you monitor the progress of your Auto Scaling group and to assist in troubleshooting any configuration issues when launching Amazon EC2 instances\. For more information, see [Verify a scaling activity for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-verify-scaling-activity.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Examples<a name="aws-properties-as-group--examples"></a>

The following examples create or make changes to an Auto Scaling group\. 

You can find additional useful examples in the following sections of the *AWS CloudFormation User Guide*:
+ For additional examples of Auto Scaling groups, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.
+ For additional examples of Amazon EC2 launch templates, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate--examples) section of the `AWS::EC2::LaunchTemplate` resources\.

### An Auto Scaling group and a launch template with a parameters section<a name="aws-properties-as-group--examples--An_Auto_Scaling_group_and_a_launch_template_with_a_parameters_section"></a>

The following example shows an Auto Scaling group\. You specify values for the `MaxSize`, `MinSize`, and `DesiredCapacity` properties\.

It also shows an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource that contains the instance configuration information for the group, which uses the `LaunchTemplate` property to specify the launch template\. The [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic function gets the ID of the `AWS::EC2::LaunchTemplate` resource `myLaunchTemplate`\. The [GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html) function gets the latest version number \(for example, `1`\) of the launch template for the `Version` property\.

This example references [parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) to specify the `ImageId` and `InstanceType` properties for the launch template and the `VPCZoneIdentifier` property for the group\. Parameters are variables that you can specify when you create or update the stack\. By default, the `ImageId` property of the launch template references the latest Amazon Linux 2 AMI from the AWS Systems Manager Parameter Store\. For more information, see [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) in the *AWS Systems Manager User Guide* and the blog post [Query for the latest Amazon Linux AMI IDs using AWS Systems Manager Parameter Store](http://aws.amazon.com/blogs/compute/query-for-the-latest-amazon-linux-ami-ids-using-aws-systems-manager-parameter-store/) on the AWS Compute Blog\.

#### JSON<a name="aws-properties-as-group--examples--An_Auto_Scaling_group_and_a_launch_template_with_a_parameters_section--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "LatestAmiId": {
            "Description": "Region specific image from the Parameter Store",
            "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
            "Default": "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
        },
        "InstanceType": {
            "Description": "Amazon EC2 instance type for the instances",
            "Type": "String",
            "AllowedValues": [
                "t3.micro",
                "t3.small",
                "t3.medium"
            ],
            "Default": "t3.micro"
        },
        "Subnets": {
            "Type": "List<AWS::EC2::Subnet::Id>",
            "Description": "A list of subnets for the Auto Scaling group"
        }
    },
    "Resources": {
        "myLaunchTemplate": {
            "Type": "AWS::EC2::LaunchTemplate",
            "Properties": {
                "LaunchTemplateName": { "Fn::Sub": "${AWS::StackName}-launch-template" },
                "LaunchTemplateData": {
                    "ImageId": { "Ref": "LatestAmiId" },
                    "InstanceType": { "Ref": "InstanceType" }
                }
            }
        },
        "myASG": {
            "Type": "AWS::AutoScaling::AutoScalingGroup",
            "Properties": {
                "LaunchTemplate": {
                    "LaunchTemplateId": { "Ref": "myLaunchTemplate" },
                    "Version": { "Fn::GetAtt": [ "myLaunchTemplate", "LatestVersionNumber" ] }
                },
                "MaxSize": "1",
                "MinSize": "0",
                "DesiredCapacity": "1",
                "VPCZoneIdentifier": { "Ref": "Subnets" }
            }
        }
    }
}
```

#### YAML<a name="aws-properties-as-group--examples--An_Auto_Scaling_group_and_a_launch_template_with_a_parameters_section--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Parameters:
  LatestAmiId:
    Description: Region specific image from the Parameter Store
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: '/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2'
  InstanceType:
    Description: Amazon EC2 instance type for the instances
    Type: String
    AllowedValues:
      - t3.micro
      - t3.small
      - t3.medium
    Default: t3.micro
  Subnets:
    Type: 'List<AWS::EC2::Subnet::Id>'
    Description: A list of subnets for the Auto Scaling group
Resources:
  myLaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties: 
      LaunchTemplateName: !Sub ${AWS::StackName}-launch-template
      LaunchTemplateData:
        ImageId: !Ref LatestAmiId
        InstanceType: !Ref InstanceType
  myASG:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      LaunchTemplate:
        LaunchTemplateId: !Ref myLaunchTemplate
        Version: !GetAtt myLaunchTemplate.LatestVersionNumber
      MaxSize: '1'
      MinSize: '0'
      DesiredCapacity: '1'
      VPCZoneIdentifier: !Ref Subnets
```

### Auto Scaling group with CloudWatch monitoring enabled and custom tags<a name="aws-properties-as-group--examples--Auto_Scaling_group_with_CloudWatch_monitoring_enabled_and_custom_tags"></a>

The following snippet shows an Auto Scaling group with CloudWatch monitoring enabled and custom tags\. The `LaunchTemplate` property references an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource with the logical name `myLaunchTemplate` that is defined elsewhere in your template\.

You specify the CloudWatch metrics to monitor using the `MetricsCollection` property\. If you keep the metrics as they are, only `GroupMinSize` and `GroupMaxSize` metrics are enabled\.

You specify the tag keys and tag key values for the `Tags` property\. If you keep the provided tags, the first tag, `Environment`=`Production`, is assigned to the Auto Scaling group and to any EC2 instances launched as part of the Auto Scaling group\. The second tag, `Purpose`=`WebServerGroup`, is assigned only to the Auto Scaling group itself\.

You also specify values for the `MaxSize`, `MinSize`, `DesiredCapacity`, and `VPCZoneIdentifier` properties\.

#### JSON<a name="aws-properties-as-group--examples--Auto_Scaling_group_with_CloudWatch_monitoring_enabled_and_custom_tags--json"></a>

```
{
    "Resources": {
        "myASG": {
            "Type": "AWS::AutoScaling::AutoScalingGroup",
            "Properties": {
                "LaunchTemplate": {
                    "LaunchTemplateId": { "Ref": "myLaunchTemplate" },
                    "Version": { "Fn::GetAtt": [ "myLaunchTemplate", "LatestVersionNumber" ] }
                },
                "MaxSize": "1",
                "MinSize": "0",
                "DesiredCapacity": "1",
                "VPCZoneIdentifier": [
                    "subnetIdAz1",
                    "subnetIdAz2",
                    "subnetIdAz3"
                ],
                "MetricsCollection": [
                    {
                        "Granularity": "1Minute",
                        "Metrics": [
                            "GroupMinSize",
                            "GroupMaxSize"
                        ]
                    }
                ],
                "Tags": [
                    {
                        "Key": "Environment",
                        "Value": "Production",
                        "PropagateAtLaunch": "true"
                    },
                    {
                        "Key": "Purpose",
                        "Value": "WebServerGroup",
                        "PropagateAtLaunch": "false"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-properties-as-group--examples--Auto_Scaling_group_with_CloudWatch_monitoring_enabled_and_custom_tags--yaml"></a>

```
---
Resources:
  myASG:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      LaunchTemplate:
        LaunchTemplateId: !Ref myLaunchTemplate
        Version: !GetAtt myLaunchTemplate.LatestVersionNumber
      MaxSize: '1'
      MinSize: '0'
      DesiredCapacity: '1'
      VPCZoneIdentifier:   
        - subnetIdAz1
        - subnetIdAz2
        - subnetIdAz3
      MetricsCollection: 
        - Granularity: 1Minute
          Metrics: 
            - GroupMinSize
            - GroupMaxSize
      Tags:
        - Key: Environment
          Value: Production
          PropagateAtLaunch: true
        - Key: Purpose
          Value: WebServerGroup
          PropagateAtLaunch: false
```

## See also<a name="aws-properties-as-group--seealso"></a>
+ [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)
+  [AWS CloudFormation stack updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) 
+ [CreateAutoScalingGroup](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CreateAutoScalingGroup.html) in the *Amazon EC2 Auto Scaling API Reference*
+ [UpdateAutoScalingGroup](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_UpdateAutoScalingGroup.html) in the *Amazon EC2 Auto Scaling API Reference*

