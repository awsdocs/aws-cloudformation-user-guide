# Amazon Elastic Compute Cloud SpotFleet LaunchTemplateOverrides<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides"></a>

`LaunchTemplateOverrides` is a property of the [Amazon EC2 SpotFleet SpotFleetRequestConfigData](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata.md) property that describes overrides for a launch template\.

## Syntax<a name="w3ab2c21c14d798b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-ec2-spotfleet-launchtemplateoverrides-availabilityzone)" : String,
  "[InstanceType](#cfn-ec2-spotfleet-launchtemplateoverrides-instancetype)" : String,
  "[SpotPrice](#cfn-ec2-spotfleet-launchtemplateoverrides-spotprice)" : String,
  "[SubnetId](#cfn-ec2-spotfleet-launchtemplateoverrides-subnetid)" : String,
  "[WeightedCapacity](#cfn-ec2-spotfleet-launchtemplateoverrides-weightedcapacity)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides-syntax.yaml"></a>

```
[AvailabilityZone](#cfn-ec2-spotfleet-launchtemplateoverrides-availabilityzone): String
[InstanceType](#cfn-ec2-spotfleet-launchtemplateoverrides-instancetype): String
[SpotPrice](#cfn-ec2-spotfleet-launchtemplateoverrides-spotprice): String
[SubnetId](#cfn-ec2-spotfleet-launchtemplateoverrides-subnetid): String
[WeightedCapacity](#cfn-ec2-spotfleet-launchtemplateoverrides-weightedcapacity): Boolean
```

## Properties<a name="w3ab2c21c14d798b7"></a>

`AvailabilityZone`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-availabilityzone"></a>
The Availability Zone in which to launch the instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceType`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-instancetype"></a>
The instance type\.  
For a complete list of valid values, see `InstanceType` in [LaunchTemplateOverrides](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateOverrides.html) in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SpotPrice`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-spotprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetId`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-subnetid"></a>
The ID of the subnet in which to launch the instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`WeightedCapacity`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-weightedcapacity"></a>
The number of units provided by the specified instance type\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)