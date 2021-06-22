# AWS::EC2::SpotFleet SpotPlacement<a name="aws-properties-ec2-spotfleet-spotplacement"></a>

Describes Spot Instance placement\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotplacement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotplacement-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-ec2-spotfleet-spotplacement-availabilityzone)" : String,
  "[GroupName](#cfn-ec2-spotfleet-spotplacement-groupname)" : String,
  "[Tenancy](#cfn-ec2-spotfleet-spotplacement-tenancy)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotplacement-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-ec2-spotfleet-spotplacement-availabilityzone): String
  [GroupName](#cfn-ec2-spotfleet-spotplacement-groupname): String
  [Tenancy](#cfn-ec2-spotfleet-spotplacement-tenancy): String
```

## Properties<a name="aws-properties-ec2-spotfleet-spotplacement-properties"></a>

`AvailabilityZone`  <a name="cfn-ec2-spotfleet-spotplacement-availabilityzone"></a>
The Availability Zone\.  
To specify multiple Availability Zones, separate them using commas; for example, "us\-west\-2a, us\-west\-2b"\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupName`  <a name="cfn-ec2-spotfleet-spotplacement-groupname"></a>
The name of the placement group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tenancy`  <a name="cfn-ec2-spotfleet-spotplacement-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of `dedicated` runs on single\-tenant hardware\. The `host` tenancy is not supported for Spot Instances\.  
*Required*: No  
*Type*: String  
*Allowed values*: `dedicated | default | host`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)