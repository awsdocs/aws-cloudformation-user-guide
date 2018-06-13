# AWS::AutoScaling::AutoScalingGroup<a name="aws-properties-as-group"></a>

Creates an Auto Scaling group\.

You can add an [UpdatePolicy](aws-attribute-updatepolicy.md) attribute to your Auto Scaling group to control how rolling updates are performed when a change has been made to the Auto Scaling group's [launch configuration](aws-properties-as-launchconfig.md) or [subnet group membership](#cfn-as-group-vpczoneidentifier)\.

**Topics**
+ [Syntax](#aws-resource-autoscaling-autoscalinggroup-syntax)
+ [Properties](#aws-properties-as-group-prop)
+ [Return Value](#aws-properties-as-group-ref)
+ [Examples](#w3ab2c21c10d130c15)
+ [See Also](#w3ab2c21c10d130c17)

## Syntax<a name="aws-resource-autoscaling-autoscalinggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-autoscalinggroup-syntax.json"></a>

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
      "[LaunchTemplate](#cfn-as-group-launchtemplate)" : [*LaunchTemplateSpecification*](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md),
      "[LifecycleHookSpecificationList](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist)" : [ [*LifecycleHookSpecification*](aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification.md), ... ],
      "[LoadBalancerNames](#cfn-as-group-loadbalancernames)" : [ String, ... ],
      "[MaxSize](#cfn-as-group-maxsize)" : String,
      "[MetricsCollection](#cfn-as-group-metricscollection)" : [ [*MetricsCollection*](aws-properties-as-metricscollection.md), ... ],
      "[MinSize](#cfn-as-group-minsize)" : String,
      "[NotificationConfigurations](#cfn-as-group-notificationconfigurations)" : [ [*NotificationConfiguration*](aws-properties-as-notificationconfigurations.md), ... ],
      "[PlacementGroup](#cfn-as-group-placementgroup)" : String,
      "[ServiceLinkedRoleARN](#cfn-autoscaling-autoscalinggroup-servicelinkedrolearn)" : String,
      "[Tags](#cfn-as-group-tags)" : [ [*TagProperty*](aws-properties-as-tags.md), ... ],
      "[TargetGroupARNs](#cfn-as-group-targetgrouparns)" : [ String, ... ],
      "[TerminationPolicies](#cfn-as-group-termpolicy)" : [ String, ... ],
      "[VPCZoneIdentifier](#cfn-as-group-vpczoneidentifier)" : [ String, ... ]
   }
}
```

### YAML<a name="aws-resource-autoscaling-autoscalinggroup-syntax.yaml"></a>

```
Type: "AWS::AutoScaling::AutoScalingGroup"
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
  [LaunchTemplate](#cfn-as-group-launchtemplate)" : [*LaunchTemplateSpecification*](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)
  [LifecycleHookSpecificationList](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist): 
    - [*LifecycleHookSpecification*](aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification.md)
  [LoadBalancerNames](#cfn-as-group-loadbalancernames):
    - String
  [MaxSize](#cfn-as-group-maxsize): String
  [MetricsCollection](#cfn-as-group-metricscollection):
    - [*MetricsCollection*](aws-properties-as-metricscollection.md)
  [MinSize](#cfn-as-group-minsize): String
  [NotificationConfigurations](#cfn-as-group-notificationconfigurations):
    - [*NotificationConfiguration*](aws-properties-as-notificationconfigurations.md)
  [PlacementGroup](#cfn-as-group-placementgroup): String
  [ServiceLinkedRoleARN](#cfn-autoscaling-autoscalinggroup-servicelinkedrolearn): String
  [Tags](#cfn-as-group-tags):
    - [*TagProperty*](aws-properties-as-tags.md)
  [TargetGroupARNs](#cfn-as-group-targetgrouparns):
    - String
  [TerminationPolicies](#cfn-as-group-termpolicy):
    - String
  [VPCZoneIdentifier](#cfn-as-group-vpczoneidentifier):
    - String
```

## Properties<a name="aws-properties-as-group-prop"></a>

`AutoScalingGroupName`  <a name="cfn-autoscaling-autoscalinggroup-autoscalinggroupname"></a>
The name of the Auto Scaling group\.  
Minimum length of 1\. Maximum length of 255\. Must follow the following pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`AvailabilityZones`  <a name="cfn-as-group-availabilityzones"></a>
Contains a list of availability zones for the group\.  
*Required*: Conditional\. If you don't specify the `VPCZoneIdentifier` property, you must specify this property\.  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Cooldown`  <a name="cfn-as-group-cooldown"></a>
The number of seconds after a scaling activity is completed before any further scaling activities can start\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DesiredCapacity`  <a name="cfn-as-group-desiredcapacity"></a>
Specifies the desired capacity for the Auto Scaling group\.  
If `SpotPrice` is not set in the [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md) for this Auto Scaling group, then Auto Scaling will begin to bring instances online based on `DesiredCapacity`\. CloudFormation will not mark the Auto Scaling group as successful \(by setting its status to CREATE\_COMPLETE\) until the desired capacity is reached\.  
If `SpotPrice` *is* set, then `DesiredCapacity` will not be used as a criteria for success, since instances will only be started when the spot price has been matched\. After the spot price has been matched, however, Auto Scaling uses `DesiredCapacity` as the target capacity for the group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckGracePeriod`  <a name="cfn-as-group-healthcheckgraceperiod"></a>
The length of time in seconds after a new EC2 instance comes into service that Auto Scaling starts checking its health\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckType`  <a name="cfn-as-group-healthchecktype"></a>
The service you want the health status from, Amazon EC2 or Elastic Load Balancer\. Valid values are `EC2` or `ELB`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceId`  <a name="cfn-as-group-instanceid"></a>
The ID of the Amazon EC2 instance you want to use to create the Auto Scaling group\. Use this property if you want to create an Auto Scaling group that uses an existing Amazon EC2 instance instead of a launch configuration\.  
When you use an Amazon EC2 instance to create an Auto Scaling group, a new launch configuration is first created and then associated with the Auto Scaling group\. The new launch configuration derives all its properties from the instance, with the exception of `BlockDeviceMapping` and `AssociatePublicIpAddress`\.  
*Required*: Conditional\. You must specify one of the following: `InstanceId`, `LaunchConfigurationName`, or `LaunchTemplate`\.   
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LaunchConfigurationName`  <a name="cfn-as-group-launchconfigurationname"></a>
Specifies the name of the associated [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md) resource\.  
If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the `DependsOn` attribute to declare a dependency on the VPC\-gateway attachment\. For more information, see [DependsOn Attribute](aws-attribute-dependson.md)\.
*Required*: Conditional\. You must specify one of the following: `InstanceId`, `LaunchConfigurationName` or `LaunchTemplate`\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
When you update the `LaunchConfigurationName`, existing Amazon EC2 instances continue to run with the configuration that they were originally launched with\. To update existing instances, specify an update policy attribute for this Auto Scaling group\. For more information, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.

`LaunchTemplate`  <a name="cfn-as-group-launchtemplate"></a>
The launch template to use to launch instances\.  
*Required*: Conditional\. You must specify one of the following: `InstanceId`, `LaunchConfigurationName`, or `LaunchTemplate`\.  
*Type*: [Amazon EC2 Auto Scaling AutoScalingGroup LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
When you update the `LaunchTemplate`, existing Amazon EC2 instances continue to run with the configuration that they were originally launched with\. To update existing instances, specify an update policy attribute for this Auto Scaling group\. For more information, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.

`LifecycleHookSpecificationList`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecificationlist"></a>
The lifecycle hooks for the group, which specify actions to perform when Auto Scaling launches or terminates instances\. For more information, see [ Amazon EC2 Auto Scaling Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: List of [Amazon EC2 Auto Scaling AutoScalingGroup LifecycleHookSpecification](aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LoadBalancerNames`  <a name="cfn-as-group-loadbalancernames"></a>
A list of Classic load balancers associated with this Auto Scaling group\. To specify Application load balancers, use `TargetGroupARNs`\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MaxSize`  <a name="cfn-as-group-maxsize"></a>
The maximum size of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricsCollection`  <a name="cfn-as-group-metricscollection"></a>
Enables the monitoring of group metrics of an Auto Scaling group\.  
*Required*: No  
*Type*: A list of [Amazon EC2 Auto Scaling AutoScalingGroup MetricsCollection](aws-properties-as-metricscollection.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MinSize`  <a name="cfn-as-group-minsize"></a>
The minimum size of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NotificationConfigurations`  <a name="cfn-as-group-notificationconfigurations"></a>
An embedded property that configures an Auto Scaling group to send notifications when specified events take place\.  
*Required*: No  
*Type*: List of [Amazon EC2 Auto Scaling AutoScalingGroup NotificationConfiguration](aws-properties-as-notificationconfigurations.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PlacementGroup`  <a name="cfn-as-group-placementgroup"></a>
The name of an existing cluster placement group into which you want to launch your instances\. A placement group is a logical grouping of instances within a single Availability Zone\. You cannot specify multiple Availability Zones and a placement group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ServiceLinkedRoleARN`  <a name="cfn-autoscaling-autoscalinggroup-servicelinkedrolearn"></a>
The Amazon Resource Name \(ARN\) of the service\-linked role that the Auto Scaling group uses to call other AWS services on your behalf\. By default, Auto Scaling uses a service\-linked role named AWSServiceRoleForAutoScaling, which it creates if it does not exist\.  
Length Constraints: Minimum length of 1\. Maximum length of 1600\.  
Pattern: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-as-group-tags"></a>
The Auto Scaling tags to attach to this resource\. For more information about Auto Scaling tags, see [Tagging Auto Scaling Groups and Instances](http://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-tagging.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: List of [Amazon EC2 Auto Scaling AutoScalingGroup TagProperty](aws-properties-as-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetGroupARNs`  <a name="cfn-as-group-targetgrouparns"></a>
A list of Amazon Resource Names \(ARN\) of target groups to associate with the Auto Scaling group\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TerminationPolicies`  <a name="cfn-as-group-termpolicy"></a>
A policy or a list of policies that are used to select the instances to terminate\. The policies are executed in the order that you list them\.  
 For more information on configuring a termination policy for your Auto Scaling group, see [Controlling Which Auto Scaling Instances Terminate During Scale In](http://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VPCZoneIdentifier`  <a name="cfn-as-group-vpczoneidentifier"></a>
A list of subnet identifiers of Amazon Virtual Private Cloud \(Amazon VPCs\)\.  
If you specify the `AvailabilityZones` property, the subnets that you specify for this property must reside in those Availability Zones\.  
For more information, see [Launching Auto Scaling Instances in a VPC](http://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-in-vpc.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: Conditional\. If you don't specify the `AvailabilityZones` property, you must specify this property\.  
*Type*: List of String values  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)  
When you update VPCZoneIdentifier, the instances are replaced, but not the Auto Scaling group\.

## Return Value<a name="aws-properties-as-group-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

In the following sample, the `Ref` function returns the name of the `MyASGroup` Auto Scaling group, such as `mystack-myasgroup-NT5EUXTNTXXD`\.

```
{ "Ref": "MyASGroup" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d130c15"></a>

To view more Auto Scaling examples, see [Auto Scaling Template Snippets](quickref-autoscaling.md)\.

### Auto Scaling Group with an Elastic Load Balancing Load Balancer, Launch Configuration, and Metric Collection<a name="w3ab2c21c10d130c15b4"></a>

#### JSON<a name="aws-resource-autoscaling-autoscalinggroup-example1.json"></a>

```
"WebServerGroup" : {
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Properties" : {
      "AvailabilityZones" : { "Fn::GetAZs" : "" },
      "LaunchConfigurationName" : { "Ref" : "LaunchConfig" },
      "MinSize" : "2",
      "MaxSize" : "2",
      "LoadBalancerNames" : [ { "Ref" : "ElasticLoadBalancer" } ],
      "MetricsCollection": [
         {
            "Granularity": "1Minute",
            "Metrics": [
               "GroupMinSize",
               "GroupMaxSize"
            ]
         }
      ]
   }
}
```

#### YAML<a name="aws-resource-autoscaling-autoscalinggroup-example1.yaml"></a>

```
WebServerGroup: 
  Type: "AWS::AutoScaling::AutoScalingGroup"
  Properties: 
    AvailabilityZones: 
      Fn::GetAZs: ""
    LaunchConfigurationName: 
      Ref: "LaunchConfig"
    MinSize: "2"
    MaxSize: "2"
    LoadBalancerNames: 
      - Ref: "ElasticLoadBalancer"
    MetricsCollection: 
      - 
        Granularity: "1Minute"
        Metrics: 
          - "GroupMinSize"
          - "GroupMaxSize"
```

### Batch Update Instances in an Auto Scaling Group<a name="w3ab2c21c10d130c15b6"></a>

The following example shows how to configure updates by including an [UpdatePolicy](aws-attribute-updatepolicy.md) attribute\. The attribute contains an `AutoScalingRollingUpdate` embedded object with three attributes that specify the update policy settings\.

```
"ASG1" : {
   "UpdatePolicy" : {
      "AutoScalingRollingUpdate" : {
         "MinInstancesInService" : "1",
         "MaxBatchSize" : "1",
         "PauseTime" : "PT12M5S"
      }
   },
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Properties" : {
      "AvailabilityZones" : { "Fn::GetAZs" : { "Ref" : "AWS::Region" } },
      "LaunchConfigurationName" : { "Ref" : "ASLC" },
      "MaxSize" : "3",
      "MinSize" : "1"
   }
}
```

### Auto Scaling Group Wait on Signals From New Instances<a name="w3ab2c21c10d130c15b8"></a>

In the following example, the Auto Scaling group waits for new Amazon EC2 instances to signal the group before Auto Scaling proceeds to update the next batch of instances\. In the [UpdatePolicy](aws-attribute-updatepolicy.md) attribute, the `WaitOnResourceSignals` flag is set to `true`\. You can use the [cfn\-signal](cfn-signal.md) helper script on each instance to signal the Auto Scaling group\.

#### JSON<a name="aws-resource-autoscaling-autoscalinggroup-example2.json"></a>

```
"ASG1" : {
   "UpdatePolicy" : {
      "AutoScalingRollingUpdate" : {
         "MinInstancesInService" : "1",
         "MaxBatchSize" : "1",
         "PauseTime" : "PT12M5S",
         "WaitOnResourceSignals" : "true"
      }
   },
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Properties" : {
      "AvailabilityZones" : { "Fn::GetAZs" : { "Ref" : "AWS::Region" } },
      "LaunchConfigurationName" : { "Ref" : "ASLC" },
      "MaxSize" : "3",
      "MinSize" : "1"
   }
}
```

#### YAML<a name="aws-resource-autoscaling-autoscalinggroup-example2.yaml"></a>

```
ASG1: 
  UpdatePolicy: 
    AutoScalingRollingUpdate: 
      MinInstancesInService: "1"
      MaxBatchSize: "1"
      PauseTime: "PT12M5S"
      WaitOnResourceSignals: "true"
  Type: "AWS::AutoScaling::AutoScalingGroup"
  Properties: 
    AvailabilityZones: 
      Fn::GetAZs: 
        Ref: "AWS::Region"
    LaunchConfigurationName: 
      Ref: "ASLC"
    MaxSize: "3"
    MinSize: "1"
```

## See Also<a name="w3ab2c21c10d130c17"></a>
+ [UpdatePolicy](aws-attribute-updatepolicy.md)
+ [UpdateAutoScalingGroup](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_UpdateAutoScalingGroup.html) in the *Amazon EC2 Auto Scaling API Reference*
+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)