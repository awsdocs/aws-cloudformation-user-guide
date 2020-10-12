# AWS::EC2::SpotFleet SpotPlacement<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement"></a>

Describes Spot Instance placement\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-ec2-spotfleet-spotplacement-availabilityzone)" : String,
  "[GroupName](#cfn-ec2-spotfleet-spotplacement-groupname)" : String,
  "[Tenancy](#cfn-ec2-spotfleet-spotplacement-tenancy)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-ec2-spotfleet-spotplacement-availabilityzone): String
  [GroupName](#cfn-ec2-spotfleet-spotplacement-groupname): String
  [Tenancy](#cfn-ec2-spotfleet-spotplacement-tenancy): String
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-properties"></a>

`AvailabilityZone`  <a name="cfn-ec2-spotfleet-spotplacement-availabilityzone"></a>
The Availability Zone\.  
To specify multiple Availability Zones, separate them using commas; for example, "us\-west\-2a, us\-west\-2b"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupName`  <a name="cfn-ec2-spotfleet-spotplacement-groupname"></a>
The name of the placement group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tenancy`  <a name="cfn-ec2-spotfleet-spotplacement-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of `dedicated` runs on single\-tenant hardware\. The `host` tenancy is not supported for Spot Instances\.  
*Required*: No  
*Type*: String  
*Allowed values*: `dedicated | default | host`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)