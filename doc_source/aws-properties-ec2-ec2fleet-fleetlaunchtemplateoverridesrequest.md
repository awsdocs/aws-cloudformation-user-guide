# Amazon EC2 EC2Fleet FleetLaunchTemplateOverridesRequest<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest"></a>

<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-description"></a>The `FleetLaunchTemplateOverridesRequest` property type specifies overrides for a launch template for an EC2 Fleet\.

<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-inheritance"></a> `FleetLaunchTemplateOverridesRequest` is a property of the [FleetLaunchTemplateConfigRequest](aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest.md) property type\.

## Syntax<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-availabilityzone)" : String,
  "[InstanceType](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-instancetype)" : String,
  "[MaxPrice](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-maxprice)" : String,
  "[Priority](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-priority)" : Double,
  "[SubnetId](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-subnetid)" : String,
  "[WeightedCapacity](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-weightedcapacity)" : Double
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-syntax.yaml"></a>

```
[AvailabilityZone](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-availabilityzone): String
[InstanceType](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-instancetype): String
[MaxPrice](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-maxprice): String
[Priority](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-priority): Double
[SubnetId](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-subnetid): String
[WeightedCapacity](#cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-weightedcapacity): Double
```

## Properties<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-properties"></a>

`AvailabilityZone`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-availabilityzone"></a>
The Availability Zone in which to launch the instances\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstanceType`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-instancetype"></a>
The instance type\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxPrice`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-maxprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Priority`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-priority"></a>
The priority for the launch template override\. If **AllocationStrategy** is set to prioritized, EC2 Fleet uses priority to determine which launch template override to use first in fulfilling On\-Demand capacity\. The highest priority is launched first\. Valid values are whole numbers starting at `0`\. The lower the number, the higher the priority\. If no number is set, the launch template override has the lowest priority\.   
 *Required*: No  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetId`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-subnetid"></a>
The ID of the subnet in which to launch the instances\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`WeightedCapacity`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-weightedcapacity"></a>
The number of units provided by the specified instance type\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest-seealso"></a>
+ [FleetLaunchTemplateOverridesRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_FleetLaunchTemplateOverridesRequest.html) in the *Amazon EC2 API Reference*