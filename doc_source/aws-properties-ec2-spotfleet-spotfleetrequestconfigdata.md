# Amazon EC2 SpotFleet SpotFleetRequestConfigData<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata"></a>

`SpotFleetRequestConfigData` is a property of the [AWS::EC2::SpotFleet](aws-resource-ec2-spotfleet.md) resource that defines the configuration of a Spot fleet request\.

## Syntax<a name="w4ab1c21c10d102d118c78b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-allocationstrategy)" : String,
  "[ExcessCapacityTerminationPolicy](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-excesscapacityterminationpolicy)" : String,
  "[IamFleetRole](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-iamfleetrole)" : String,
  "[InstanceInterruptionBehavior](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-instanceinterruptionbehavior)" : String,
  "[LaunchSpecifications](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications)" : [ [*LaunchSpecifications*](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md), ... ],
  "[LaunchTemplateConfigs](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchtemplateconfigs)" : [ [*LaunchTemplateConfigs*](aws-properties-ec2-spotfleet-launchtemplateconfig.md), ... ],
  "[LoadBalancersConfig](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-loadbalancersconfig)" : [*LoadBalancersConfig*](aws-properties-ec2-spotfleet-loadbalancersconfig.md),
  "[ReplaceUnhealthyInstances](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-replaceunhealthyinstances)" : Boolean,
  "[SpotPrice](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-spotprice)" : String,
  "[TargetCapacity](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-targetcapacity)" : Integer,
  "[TerminateInstancesWithExpiration](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-terminateinstanceswithexpiration)" : Boolean,
  "[Type](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-type)" : String,
  "[ValidFrom](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validfrom)" : String,
  "[ValidUntil](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validuntil)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-syntax.yaml"></a>

```
[AllocationStrategy](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-allocationstrategy): String
[ExcessCapacityTerminationPolicy](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-excesscapacityterminationpolicy): String
[IamFleetRole](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-iamfleetrole): String
[InstanceInterruptionBehavior](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-instanceinterruptionbehavior): String
[LaunchSpecifications](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications):
  - [*LaunchSpecifications*](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md)
[LaunchTemplateConfigs](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchtemplateconfigs):
  - [*LaunchTemplateConfigs*](aws-properties-ec2-spotfleet-launchtemplateconfig.md)
[LoadBalancersConfig](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-loadbalancersconfig): 
  [*LoadBalancersConfig*](aws-properties-ec2-spotfleet-loadbalancersconfig.md)
[ReplaceUnhealthyInstances](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-replaceunhealthyinstances): Boolean
[SpotPrice](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-spotprice): String
[TargetCapacity](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-targetcapacity): Integer
[TerminateInstancesWithExpiration](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-terminateinstanceswithexpiration): Boolean
[Type](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-type): String
[ValidFrom](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validfrom): String
[ValidUntil](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validuntil): String
```

## Properties<a name="w4ab1c21c10d102d118c78b7"></a>

For more information, including property defaults, valid values, and constraints, see [SpotFleetRequestConfigData](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotFleetRequestConfigData.html) in the *Amazon EC2 API Reference*\.

`AllocationStrategy`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-allocationstrategy"></a>
Indicates how to allocate the target capacity across the Spot pools that you specified in the Spot fleet request\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ExcessCapacityTerminationPolicy`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-excesscapacityterminationpolicy"></a>
Indicates whether running Spot instances are terminated if you decrease the target capacity of the Spot fleet request below the current size of the Spot fleet\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IamFleetRole`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-iamfleetrole"></a>
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that grants the Spot fleet the ability to bid on, launch, and terminate instances on your behalf\. For more information, see [Spot Fleet Prerequisites](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet-requests.html#spot-fleet-prerequisites) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceInterruptionBehavior`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-instanceinterruptionbehavior"></a>
The behavior when a Spot Instance is interrupted\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LaunchSpecifications`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications"></a>
The launch specifications for the Spot fleet request\.  
*Required*: Conditional\. You must specify either `LaunchSpecifications` or `LaunchTemplateConfigs`\.  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LaunchTemplateConfigs`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchtemplateconfigs"></a>
Describes a launch template and overrides\.  
*Required*: Conditional\. You must specify either `LaunchSpecifications` or `LaunchTemplateConfigs`\.  
*Type*: List of [LaunchTemplateConfig](aws-properties-ec2-spotfleet-launchtemplateconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LoadBalancersConfig`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-loadbalancersconfig"></a>
One or more Classic Load Balancers and target groups to attach to the Spot Fleet request\. Spot Fleet registers the running Spot Instances with the specified Classic Load Balancers and target groups\.  
*Required*: No  
*Type*: [LoadBalancersConfig](aws-properties-ec2-spotfleet-loadbalancersconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ReplaceUnhealthyInstances`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-replaceunhealthyinstances"></a>
Indicates whether the Spot fleet should replace unhealthy instances\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SpotPrice`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-spotprice"></a>
The bid price per unit hour\. For more information, see [How Spot Fleet Works](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TargetCapacity`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-targetcapacity"></a>
The number of units to request for the spot fleet\. You can choose to set the target capacity as the number of instances or as a performance characteristic that is important to your application workload, such as vCPUs, memory, or I/O\. For more information, see [How Spot Fleet Works](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TerminateInstancesWithExpiration`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-terminateinstanceswithexpiration"></a>
Indicates whether running Spot instances are terminated when the Spot fleet request expires\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Type`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-type"></a>
The type of request, which indicates whether the fleet will only request the target capacity or also attempt to maintain it\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ValidFrom`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-validfrom"></a>
The start date and time of the request, in UTC format \(*YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. By default, Amazon Elastic Compute Cloud \(Amazon EC2 \) starts fulfilling the request immediately\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ValidUntil`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-validuntil"></a>
The end date and time of the request, in UTC format \(*YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. After the end date and time, Amazon EC2 doesn't request new Spot instances or enable them to fulfill the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)