# AWS::EC2::SpotFleet LaunchTemplateOverrides<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides"></a>

Specifies overrides for a launch template\.

## Syntax<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-ec2-spotfleet-launchtemplateoverrides-availabilityzone)" : String,
  "[InstanceType](#cfn-ec2-spotfleet-launchtemplateoverrides-instancetype)" : String,
  "[SpotPrice](#cfn-ec2-spotfleet-launchtemplateoverrides-spotprice)" : String,
  "[SubnetId](#cfn-ec2-spotfleet-launchtemplateoverrides-subnetid)" : String,
  "[WeightedCapacity](#cfn-ec2-spotfleet-launchtemplateoverrides-weightedcapacity)" : Double
}
```

### YAML<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-ec2-spotfleet-launchtemplateoverrides-availabilityzone): String
  [InstanceType](#cfn-ec2-spotfleet-launchtemplateoverrides-instancetype): String
  [SpotPrice](#cfn-ec2-spotfleet-launchtemplateoverrides-spotprice): String
  [SubnetId](#cfn-ec2-spotfleet-launchtemplateoverrides-subnetid): String
  [WeightedCapacity](#cfn-ec2-spotfleet-launchtemplateoverrides-weightedcapacity): Double
```

## Properties<a name="aws-properties-ec2-spotfleet-launchtemplateoverrides-properties"></a>

`AvailabilityZone`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-availabilityzone"></a>
The Availability Zone in which to launch the instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-instancetype"></a>
The instance type\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `a1.2xlarge | a1.4xlarge | a1.large | a1.medium | a1.xlarge | c1.medium | c1.xlarge | c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.18xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.xlarge | c5d.18xlarge | c5d.2xlarge | c5d.4xlarge | c5d.9xlarge | c5d.large | c5d.xlarge | c5n.18xlarge | c5n.2xlarge | c5n.4xlarge | c5n.9xlarge | c5n.large | c5n.xlarge | cc1.4xlarge | cc2.8xlarge | cg1.4xlarge | cr1.8xlarge | d2.2xlarge | d2.4xlarge | d2.8xlarge | d2.xlarge | f1.16xlarge | f1.2xlarge | f1.4xlarge | g2.2xlarge | g2.8xlarge | g3.16xlarge | g3.4xlarge | g3.8xlarge | g3s.xlarge | h1.16xlarge | h1.2xlarge | h1.4xlarge | h1.8xlarge | hi1.4xlarge | hs1.8xlarge | i2.2xlarge | i2.4xlarge | i2.8xlarge | i2.xlarge | i3.16xlarge | i3.2xlarge | i3.4xlarge | i3.8xlarge | i3.large | i3.metal | i3.xlarge | m1.large | m1.medium | m1.small | m1.xlarge | m2.2xlarge | m2.4xlarge | m2.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.16xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.large | m5.metal | m5.xlarge | m5a.12xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.large | m5a.xlarge | m5ad.12xlarge | m5ad.16xlarge | m5ad.24xlarge | m5ad.2xlarge | m5ad.4xlarge | m5ad.8xlarge | m5ad.large | m5ad.xlarge | m5d.12xlarge | m5d.24xlarge | m5d.2xlarge | m5d.4xlarge | m5d.large | m5d.metal | m5d.xlarge | p2.16xlarge | p2.8xlarge | p2.xlarge | p3.16xlarge | p3.2xlarge | p3.8xlarge | p3dn.24xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.large | r5.metal | r5.xlarge | r5a.12xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.large | r5a.xlarge | r5ad.12xlarge | r5ad.16xlarge | r5ad.24xlarge | r5ad.2xlarge | r5ad.4xlarge | r5ad.8xlarge | r5ad.large | r5ad.xlarge | r5d.12xlarge | r5d.24xlarge | r5d.2xlarge | r5d.4xlarge | r5d.large | r5d.metal | r5d.xlarge | t1.micro | t2.2xlarge | t2.large | t2.medium | t2.micro | t2.nano | t2.small | t2.xlarge | t3.2xlarge | t3.large | t3.medium | t3.micro | t3.nano | t3.small | t3.xlarge | t3a.2xlarge | t3a.large | t3a.medium | t3a.micro | t3a.nano | t3a.small | t3a.xlarge | u-12tb1.metal | u-6tb1.metal | u-9tb1.metal | x1.16xlarge | x1.32xlarge | x1e.16xlarge | x1e.2xlarge | x1e.32xlarge | x1e.4xlarge | x1e.8xlarge | x1e.xlarge | z1d.12xlarge | z1d.2xlarge | z1d.3xlarge | z1d.6xlarge | z1d.large | z1d.metal | z1d.xlarge`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotPrice`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-spotprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-subnetid"></a>
The ID of the subnet in which to launch the instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeightedCapacity`  <a name="cfn-ec2-spotfleet-launchtemplateoverrides-weightedcapacity"></a>
The number of units provided by the specified instance type\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)