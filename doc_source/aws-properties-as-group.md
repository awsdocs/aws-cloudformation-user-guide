# AWS::AutoScaling::AutoScalingGroup<a name="aws-properties-as-group"></a>

Defines an Amazon EC2 Auto Scaling group with the specified name and attributes\. 

To configure Amazon EC2 instances launched as part of the group, you can specify a launch template or a launch configuration\. We recommend that you use a launch template to make sure that you can use the latest features of Amazon EC2, such as Dedicated Hosts and T2 Unlimited instances\. For more information, see [Creating a Launch Template for an Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html)\.

You can add an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) to your Auto Scaling group to perform rolling updates \(or replace the group\) when a change has been made to the group\. You can find sample update policies for rolling updates in the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#aws-properties-as-group--examples) section\.

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
A list of Availability Zones for the group\. You must specify one of the following properties: `VPCZoneIdentifier` or `AvailabilityZones`\.   
If your account supports EC2\-Classic and VPC, this property is required to create an Auto Scaling group that launches instances into EC2\-Classic\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cooldown`  <a name="cfn-as-group-cooldown"></a>
The amount of time, in seconds, after a scaling activity completes before another scaling activity can start\. The default value is `300`\.   
This setting applies when using simple scaling policies, but not when using other scaling policies or scheduled scaling\. For more information, see [Scaling Cooldowns for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/Cooldown.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredCapacity`  <a name="cfn-as-group-desiredcapacity"></a>
The desired capacity is the initial capacity of the Auto Scaling group at the time of its creation and the capacity it attempts to maintain\. It can scale beyond this capacity if you configure automatic scaling\.  
The number must be greater than or equal to the minimum size of the group and less than or equal to the maximum size of the group\. If you do not specify a desired capacity, the default is the minimum size of the group\.  
CloudFormation marks the Auto Scaling group as successful \(by setting its status to CREATE\_COMPLETE\) when the desired capacity is reached\. However, if `SpotPrice` is set in the [launch configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html), then desired capacity is not used as a criteria for success, because whether your request is fulfilled depends on Spot Instance capacity and your maximum price\. If the current Spot price is less than your specified maximum price, Amazon EC2 Auto Scaling uses `DesiredCapacity` as the target capacity for the group\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckGracePeriod`  <a name="cfn-as-group-healthcheckgraceperiod"></a>
The amount of time, in seconds, that Amazon EC2 Auto Scaling waits before checking the health status of an EC2 instance that has come into service\.   
If you don't specify a value, AWS CloudFormation uses the API default value of `0` seconds\.  
For more information, see [Health Checks for Auto Scaling Instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
If you are adding an `ELB` health check, you must specify this property\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckType`  <a name="cfn-as-group-healthchecktype"></a>
The service to use for the health checks\. The valid values are `EC2` \(default\) and `ELB`\. If you configure an Auto Scaling group to use ELB health checks, it considers the instance unhealthy if it fails either the EC2 status checks or the load balancer health checks\.  
For more information, see [Health Checks for Auto Scaling Instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-as-group-instanceid"></a>
The ID of the instance used to create a launch configuration for the group\.   
When you specify an ID of an instance, Amazon EC2 Auto Scaling creates a new launch configuration and associates it with the Auto Scaling group\. The new launch configuration derives all its properties from the instance, with the exception of `BlockDeviceMapping` and `AssociatePublicIpAddress`\.   
For more information, see [Create an Auto Scaling Group Using an EC2 Instance](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-asg-from-instance.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
You must specify one of the following properties: `LaunchConfigurationName`, `LaunchTemplate`, `InstanceId`, or `MixedInstancesPolicy`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchConfigurationName`  <a name="cfn-as-group-launchconfigurationname"></a>
The name of the [launch configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) to use to launch instances\.  
You must specify one of the following properties: `LaunchConfigurationName`, `LaunchTemplate`, `InstanceId`, or `MixedInstancesPolicy`\.  
When you update `LaunchConfigurationName`, existing Amazon EC2 instances continue to run with the configuration that they were originally launched with\. To update existing instances, specify an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for the Auto Scaling group\. 
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplate`  <a name="cfn-as-group-launchtemplate"></a>
Parameters used to specify the [launch template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) and version to use when an instance is launched\.  
You must specify one of the following properties: `LaunchConfigurationName`, `LaunchTemplate`, `InstanceId`, or `MixedInstancesPolicy`\.  
When you update `LaunchTemplate`, existing Amazon EC2 instances continue to run with the configuration that they were originally launched with\. To update existing instances, specify an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for the Auto Scaling group\.
*Required*: Conditional  
*Type*: [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleHookSpecificationList`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist"></a>
The lifecycle hooks for the group, which specify actions to perform when Amazon EC2 Auto Scaling launches or terminates instances\.  
*Required*: No  
*Type*: List of [LifecycleHookSpecification](aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerNames`  <a name="cfn-as-group-loadbalancernames"></a>
A list of Classic Load Balancers associated with this Auto Scaling group\. For Application Load Balancers and Network Load Balancers, specify a list of target groups using the `TargetGroupARNs` property instead\.   
For more information, see [Using a Load Balancer with an Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-load-balancer.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxInstanceLifetime`  <a name="cfn-as-group-maxinstancelifetime"></a>
The maximum amount of time, in seconds, that an instance can be in service\.  
You must specify a value of at least 604,800 seconds \(7 days\)\.  
For more information, see [Replacing Auto Scaling Instances Based on Maximum Instance Lifetime](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-max-instance-lifetime.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-as-group-maxsize"></a>
The maximum size of the Auto Scaling group\.  
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
The minimum size of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MixedInstancesPolicy`  <a name="cfn-as-group-mixedinstancespolicy"></a>
An embedded object that specifies a mixed instances policy\.  
The policy includes properties that not only define the distribution of On\-Demand Instances and Spot Instances, the maximum price to pay for Spot Instances, and how the Auto Scaling group allocates instance types to fulfill On\-Demand and Spot capacity, but also the properties that specify the instance configuration information—the launch template and instance types\.  
For more information, see [Auto Scaling Groups with Multiple Instance Types and Purchase Options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-purchase-options.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
You must specify one of the following properties: `LaunchConfigurationName`, `LaunchTemplate`, `InstanceId`, or `MixedInstancesPolicy`\.  
*Required*: Conditional  
*Type*: [MixedInstancesPolicy](aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NewInstancesProtectedFromScaleIn`  <a name="cfn-as-group-newinstancesprotectedfromscalein"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationConfigurations`  <a name="cfn-as-group-notificationconfigurations"></a>
Configures an Auto Scaling group to send notifications when specified events take place\.  
*Required*: No  
*Type*: List of [NotificationConfiguration](aws-properties-as-notificationconfigurations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementGroup`  <a name="cfn-as-group-placementgroup"></a>
The name of an existing cluster placement group into which you want to launch your instances\. A placement group is a logical grouping of instances within a single Availability Zone\. You cannot specify multiple Availability Zones and a placement group\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceLinkedRoleARN`  <a name="cfn-autoscaling-autoscalinggroup-servicelinkedrolearn"></a>
The Amazon Resource Name \(ARN\) of the service\-linked role that the Auto Scaling group uses to call other AWS services on your behalf\. By default, Amazon EC2 Auto Scaling uses a service\-linked role named AWSServiceRoleForAutoScaling, which it creates if it does not exist\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-as-group-tags"></a>
One or more tags\. You can tag your Auto Scaling group and propagate the tags to the Amazon EC2 instances it launches\.  
*Required*: No  
*Type*: List of [TagProperty](aws-properties-as-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupARNs`  <a name="cfn-as-group-targetgrouparns"></a>
A list of Amazon Resource Names \(ARN\) of target groups to associate with the Auto Scaling group\. Instances are registered as targets in a target group, and traffic is routed to the target group\.   
For more information, see [Using a Load Balancer with an Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-load-balancer.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminationPolicies`  <a name="cfn-as-group-termpolicy"></a>
A policy or a list of policies that are used to select the instances to terminate\. The policies are executed in the order that you list them\. The termination policies supported by Amazon EC2 Auto Scaling: `OldestInstance`, `OldestLaunchConfiguration`, `NewestInstance`, `ClosestToNextInstanceHour`, `Default`, `OldestLaunchTemplate`, and `AllocationStrategy`\.   
For more information, see [Controlling Which Auto Scaling Instances Terminate During Scale In](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCZoneIdentifier`  <a name="cfn-as-group-vpczoneidentifier"></a>
A list of subnet IDs for a virtual private cloud \(VPC\)\. If you specify `VPCZoneIdentifier` with `AvailabilityZones`, the subnets that you specify for this property must reside in those Availability Zones\.   
If your account supports EC2\-Classic and VPC, this property is required to create an Auto Scaling group that launches instances into a VPC\.   
If this resource has a public IP address and is also in a VPC that is defined in the same stack template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the [VPC\-gateway attachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-gateway-attachment.html)\.  
When you update `VPCZoneIdentifier`, this retains the same Auto Scaling group and replaces old instances with new ones, according to the specified subnets\. You can specify how AWS CloudFormation handles these updates by using an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.
*Required*: Conditional  
*Type*: List of String  
*Minimum*: `1`  
*Maximum*: `2047`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

## Return values<a name="aws-properties-as-group-return-values"></a>

### Ref<a name="aws-properties-as-group-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-myasgroup-NT5EUXTNTXXD`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-properties-as-group--examples"></a>

The following examples create or make changes to an Auto Scaling group\. To view more examples, see [Auto Scaling Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

### Auto Scaling Group and Launch Template<a name="aws-properties-as-group--examples--Auto_Scaling_Group_and_Launch_Template"></a>

The following example creates an Auto Scaling group and a launch template \([AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)\) that the Auto Scaling group uses to launch EC2 instances\. It uses the [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html) intrinsic function to customize the name of the launch template to include the stack name\.

The launch template provisions T2 instances in unlimited mode using the `CPUCredits` property\. By referencing a [parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) value for `ImageId`, the AMI is specified when launching the stack\. A block device mapping specifies an EBS volume to attach to each instance, in addition to attaching the volumes specified by the AMI\. Because `Monitoring` is enabled, EC2 metric data will be available at 1\-minute intervals \(known as detailed monitoring\) through CloudWatch\. 

The example stack creates an Auto Scaling group with a minimum size of 1 and a maximum size of 6\. The initial size of the group is 2 based on the value for `DesiredCapacity`\. The `VPCZoneIdentifier` property specifies the subnets where the instances will be created\. Each instance has 300 seconds to warm up before receiving its first health check\. 

#### JSON<a name="aws-properties-as-group--examples--Auto_Scaling_Group_and_Launch_Template--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "myImageId":{
      "Type":"AWS::EC2::Image::Id"
    }
  },
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
          "ImageId":{"Ref":"myImageId"},
          "KeyName":"my-key-pair-useast2",
          "InstanceType":"t2.micro",
          "Monitoring":{"Enabled":true},
          "SecurityGroupIds":["sg-7c227019", "sg-903004f8"]
        }
      }
    },
    "myASG":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "AutoScalingGroupName":"myASG",
        "MinSize":1,
        "MaxSize":6,
        "DesiredCapacity":2,
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
        "VPCZoneIdentifier":["subnet-5ea0c127", "subnet-6194ea3b", "subnet-c934b782"]
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-group--examples--Auto_Scaling_Group_and_Launch_Template--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Parameters:
  myImageId:
    Type: AWS::EC2::Image::Id
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
        ImageId: !Ref myImageId
        InstanceType: t2.micro
        KeyName: my-key-pair-useast2
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
        - subnet-5ea0c127
        - subnet-6194ea3b
        - subnet-c934b782
```

### Auto Scaling Group with Load Balancer and Multiple Properties<a name="aws-properties-as-group--examples--Auto_Scaling_Group_with_Load_Balancer_and_Multiple_Properties"></a>

The following example attaches an Elastic Load Balancing load balancer to an Auto Scaling group named `myASG`\. It enables two group metrics using the `MetricsCollection` property and creates tags using the `Tags` property\. The first tag, `Environment`=`Production`, is assigned to the Auto Scaling group and to any EC2 instances launched as part of the Auto Scaling group\. The second tag, `Purpose`=`WebServerGroup`, is assigned only to the Auto Scaling group itself\. 

It also specifies the launch configuration that the Auto Scaling group uses to launch EC2 instances\. The `AvailabilityZones` property specifies the Availability Zones where the Auto Scaling group's instances will be created\. The [Fn::GetAZs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getavailabilityzones.html) function call \{ "Fn::GetAZs" : "" \} specifies all Availability Zones for the region in which the stack is created\. Amazon EC2 Auto Scaling can scale the number of instances in the group at a minimum of 1 instance and a maximum of 4 based on the values for `MinSize` and `MaxSize`\.

#### JSON<a name="aws-properties-as-group--examples--Auto_Scaling_Group_with_Load_Balancer_and_Multiple_Properties--json"></a>

```
{
  "myASG":{
    "Type":"AWS::AutoScaling::AutoScalingGroup",
    "Properties":{
      "AvailabilityZones":{
        "Fn::GetAZs":""
      },
      "LaunchConfigurationName":{
        "Ref":"myLaunchConfig"
      },
      "MinSize":"1",
      "MaxSize":"4",
      "LoadBalancerNames":[
        {
          "Ref":"myLoadBalancer"
        }
      ],
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
```

#### YAML<a name="aws-properties-as-group--examples--Auto_Scaling_Group_with_Load_Balancer_and_Multiple_Properties--yaml"></a>

```
---
myASG: 
  Type: AWS::AutoScaling::AutoScalingGroup
  Properties: 
    AvailabilityZones: 
      Fn::GetAZs: ""
    LaunchConfigurationName: 
      Ref: "myLaunchConfig"
    MinSize: "1"
    MaxSize: "4"
    LoadBalancerNames: 
      - Ref: "myLoadBalancer"
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

### Rolling Updates with Batch Update Policy<a name="aws-properties-as-group--examples--Rolling_Updates_with_Batch_Update_Policy"></a>

The following example specifies an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for an Auto Scaling group and configures it to use the `AutoScalingRollingUpdate` policy with attributes that define the update policy settings\. 

The sample update policy instructs CloudFormation to perform a rolling update\. The rolling update makes changes to the Auto Scaling group in small batches \(for this example, instance by instance\) based on the `MaxBatchSize` and a pause time between batches of updates based on the `PauseTime`\. The `MinInstancesInService` specifies the minimum number of instances that must be in service within the Auto Scaling group while CloudFormation updates old instances\. 

While the stack update is in progress, the following Auto Scaling processes are suspended: `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, and `ScheduledActions`\. Note: Do not suspend the `Launch`, `Terminate`, or `AddToLoadBalancer` \(if the Auto Scaling group is being used with Elastic Load Balancing\) process types because it can prevent the rolling update from functioning properly\. 

#### JSON<a name="aws-properties-as-group--examples--Rolling_Updates_with_Batch_Update_Policy--json"></a>

```
{
  "myASG":{
    "UpdatePolicy":{
      "AutoScalingRollingUpdate":{
        "MinInstancesInService":"1",
        "MaxBatchSize":"1",
        "PauseTime":"PT12M5S",
        "SuspendProcesses":[
          "HealthCheck",
          "ReplaceUnhealthy",
          "AZRebalance",
          "AlarmNotification",
          "ScheduledActions"
        ]
      }
    },
    "Type":"AWS::AutoScaling::AutoScalingGroup",
    "Properties":{
      "AvailabilityZones":{
        "Fn::GetAZs":{
          "Ref":"AWS::Region"
        }
      },
      "LaunchConfigurationName":{
        "Ref":"myLaunchConfig"
      },
      "MaxSize":"3",
      "MinSize":"1"
    }
  }
}
```

#### YAML<a name="aws-properties-as-group--examples--Rolling_Updates_with_Batch_Update_Policy--yaml"></a>

```
---
myASG: 
  UpdatePolicy: 
    AutoScalingRollingUpdate: 
      MinInstancesInService: "1"
      MaxBatchSize: "1"
      PauseTime: "PT12M5S"
      SuspendProcesses:
        - HealthCheck
        - ReplaceUnhealthy
        - AZRebalance
        - AlarmNotification
        - ScheduledActions
  Type: AWS::AutoScaling::AutoScalingGroup
  Properties: 
    AvailabilityZones: 
      Fn::GetAZs: 
        Ref: "AWS::Region"
    LaunchConfigurationName: 
      Ref: "myLaunchConfig"
    MaxSize: "3"
    MinSize: "1"
```

### Batch Update Policy with Wait Condition<a name="aws-properties-as-group--examples--Batch_Update_Policy_with_Wait_Condition"></a>

The following example demonstrates a batch update policy that instructs CloudFormation to wait for new instances to signal the Auto Scaling group before the group proceeds to update the next batch of instances\. In the [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html), the `WaitOnResourceSignals` attribute is set to `true`\. CloudFormation must receive a signal from each new instance within the specified `PauseTime` before continuing the update\. To signal the Auto Scaling group, a [cfn\-signal](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-signal.html) helper script \(not shown\) is run on each instance\. 

#### JSON<a name="aws-properties-as-group--examples--Batch_Update_Policy_with_Wait_Condition--json"></a>

```
{
  "myASG":{
    "UpdatePolicy":{
      "AutoScalingRollingUpdate":{
        "MinInstancesInService":"1",
        "MaxBatchSize":"1",
        "PauseTime":"PT15M",
        "WaitOnResourceSignals":"true",
        "SuspendProcesses":[
          "HealthCheck",
          "ReplaceUnhealthy",
          "AZRebalance",
          "AlarmNotification",
          "ScheduledActions"
        ]
      }
    },
    "Type":"AWS::AutoScaling::AutoScalingGroup",
    "Properties":{
      "AvailabilityZones":{
        "Fn::GetAZs":{
          "Ref":"AWS::Region"
        }
      },
      "LaunchConfigurationName":{
        "Ref":"myLaunchConfig"
      },
      "MaxSize":"3",
      "MinSize":"1"
    }
  }
}
```

#### YAML<a name="aws-properties-as-group--examples--Batch_Update_Policy_with_Wait_Condition--yaml"></a>

```
---
myASG: 
  UpdatePolicy: 
    AutoScalingRollingUpdate: 
      MinInstancesInService: "1"
      MaxBatchSize: "1"
      PauseTime: "PT15M"
      WaitOnResourceSignals: "true"
      SuspendProcesses:
        - HealthCheck
        - ReplaceUnhealthy
        - AZRebalance
        - AlarmNotification
        - ScheduledActions
  Type: AWS::AutoScaling::AutoScalingGroup
  Properties: 
    AvailabilityZones: 
      Fn::GetAZs: 
        Ref: "AWS::Region"
    LaunchConfigurationName: 
      Ref: "myLaunchConfig"
    MaxSize: "3"
    MinSize: "1"
```

## See also<a name="aws-properties-as-group--seealso"></a>
+ [UpdatePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)
+ [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)
+ [Suspending and Resuming Scaling Processes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-suspend-resume-processes.html) in the *Amazon EC2 Auto Scaling User Guide*