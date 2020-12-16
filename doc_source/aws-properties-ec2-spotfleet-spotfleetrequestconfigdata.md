# AWS::EC2::SpotFleet SpotFleetRequestConfigData<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata"></a>

Specifies the configuration of a Spot Fleet request\. For more information, see [How Spot Fleet Works](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.

You must specify either `LaunchSpecifications` or `LaunchTemplateConfigs`\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-allocationstrategy)" : String,
  "[ExcessCapacityTerminationPolicy](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-excesscapacityterminationpolicy)" : String,
  "[IamFleetRole](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-iamfleetrole)" : String,
  "[InstanceInterruptionBehavior](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-instanceinterruptionbehavior)" : String,
  "[LaunchSpecifications](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications)" : [ SpotFleetLaunchSpecification, ... ],
  "[LaunchTemplateConfigs](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchtemplateconfigs)" : [ LaunchTemplateConfig, ... ],
  "[LoadBalancersConfig](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-loadbalancersconfig)" : LoadBalancersConfig,
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
    - SpotFleetLaunchSpecification
  [LaunchTemplateConfigs](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchtemplateconfigs): 
    - LaunchTemplateConfig
  [LoadBalancersConfig](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-loadbalancersconfig): 
    LoadBalancersConfig
  [ReplaceUnhealthyInstances](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-replaceunhealthyinstances): Boolean
  [SpotPrice](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-spotprice): String
  [TargetCapacity](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-targetcapacity): Integer
  [TerminateInstancesWithExpiration](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-terminateinstanceswithexpiration): Boolean
  [Type](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-type): String
  [ValidFrom](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validfrom): String
  [ValidUntil](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validuntil): String
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-properties"></a>

`AllocationStrategy`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-allocationstrategy"></a>
Indicates how to allocate the target Spot Instance capacity across the Spot Instance pools specified by the Spot Fleet request\.  
If the allocation strategy is `lowestPrice`, Spot Fleet launches instances from the Spot Instance pools with the lowest price\. This is the default allocation strategy\.  
If the allocation strategy is `diversified`, Spot Fleet launches instances from all the Spot Instance pools that you specify\.  
If the allocation strategy is `capacityOptimized`, Spot Fleet launches instances from Spot Instance pools with optimal capacity for the number of instances that are launching\.  
*Required*: No  
*Type*: String  
*Allowed values*: `capacityOptimized | diversified | lowestPrice`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExcessCapacityTerminationPolicy`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-excesscapacityterminationpolicy"></a>
Indicates whether running Spot Instances should be terminated if you decrease the target capacity of the Spot Fleet request below the current size of the Spot Fleet\.  
*Required*: No  
*Type*: String  
*Allowed values*: `default | noTermination`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamFleetRole`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-iamfleetrole"></a>
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that grants the Spot Fleet the permission to request, launch, terminate, and tag instances on your behalf\. For more information, see [Spot Fleet Prerequisites](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet-requests.html#spot-fleet-prerequisites) in the *Amazon EC2 User Guide for Linux Instances*\. Spot Fleet can terminate Spot Instances on your behalf when you cancel its Spot Fleet request or when the Spot Fleet request expires, if you set `TerminateInstancesWithExpiration`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceInterruptionBehavior`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-instanceinterruptionbehavior"></a>
The behavior when a Spot Instance is interrupted\. The default is `terminate`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `hibernate | stop | terminate`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchSpecifications`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications"></a>
The launch specifications for the Spot Fleet request\. If you specify `LaunchSpecifications`, you can't specify `LaunchTemplateConfigs`\.  
*Required*: Conditional  
*Type*: List of [SpotFleetLaunchSpecification](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchTemplateConfigs`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchtemplateconfigs"></a>
The launch template and overrides\. If you specify `LaunchTemplateConfigs`, you can't specify `LaunchSpecifications`\.  
*Required*: Conditional  
*Type*: List of [LaunchTemplateConfig](aws-properties-ec2-spotfleet-launchtemplateconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoadBalancersConfig`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-loadbalancersconfig"></a>
One or more Classic Load Balancers and target groups to attach to the Spot Fleet request\. Spot Fleet registers the running Spot Instances with the specified Classic Load Balancers and target groups\.  
With Network Load Balancers, Spot Fleet cannot register instances that have the following instance types: C1, CC1, CC2, CG1, CG2, CR1, CS1, G1, G2, HI1, HS1, M1, M2, M3, and T1\.  
*Required*: No  
*Type*: [LoadBalancersConfig](aws-properties-ec2-spotfleet-loadbalancersconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplaceUnhealthyInstances`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-replaceunhealthyinstances"></a>
Indicates whether Spot Fleet should replace unhealthy instances\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpotPrice`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-spotprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\. The default is the On\-Demand price\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetCapacity`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-targetcapacity"></a>
The number of units to request for the Spot Fleet\. You can choose to set the target capacity in terms of instances or a performance characteristic that is important to your application workload, such as vCPUs, memory, or I/O\. If the request type is `maintain`, you can specify a target capacity of 0 and add capacity later\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminateInstancesWithExpiration`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-terminateinstanceswithexpiration"></a>
Indicates whether running Spot Instances are terminated when the Spot Fleet request expires\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-type"></a>
The type of request\. Indicates whether the Spot Fleet only requests the target capacity or also attempts to maintain it\. When this value is `request`, the Spot Fleet only places the required requests\. It does not attempt to replenish Spot Instances if capacity is diminished, nor does it submit requests in alternative Spot pools if capacity is not available\. When this value is `maintain`, the Spot Fleet maintains the target capacity\. The Spot Fleet places the required requests to meet capacity and automatically replenishes any interrupted instances\. Default: `maintain`\. `instant` is listed but is not used by Spot Fleet\.  
*Required*: No  
*Type*: String  
*Allowed values*: `instant | maintain | request`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidFrom`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-validfrom"></a>
The start date and time of the request, in UTC format \(*YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. By default, Amazon EC2 starts fulfilling the request immediately\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidUntil`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-validuntil"></a>
The end date and time of the request, in UTC format \(*YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. After the end date and time, no new Spot Instance requests are placed or able to fulfill the request\. If no value is specified, the Spot Fleet request remains until you cancel it\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)