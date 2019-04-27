# Amazon Elastic Compute Cloud SpotFleet Placement<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement"></a>

`Placement` is a property of the [Amazon Elastic Compute Cloud SpotFleet LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that defines the placement group for the Spot instances\.

## Syntax<a name="w2922ab1c21c10c96d122c65b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone)" : String,
  "[GroupName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname)" : String,
  "[Tenancy](#cfn-ec2-spotfleet-spotplacement-tenancy)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.yaml"></a>

```
[AvailabilityZone](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone): String
[GroupName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname): String
[Tenancy](#cfn-ec2-spotfleet-spotplacement-tenancy): String
```

## Properties<a name="w2922ab1c21c10c96d122c65b7"></a>

For more information, including defaults, valid values, and constraints, see [SpotPlacement](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotPlacement.html) in the *Amazon EC2 API Reference*

`AvailabilityZone`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone"></a>
The Availability Zone \(AZ\) of the placement group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`GroupName`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname"></a>
The name of the placement group \(for cluster instances\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tenancy`  <a name="cfn-ec2-spotfleet-spotplacement-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of dedicated runs on single\-tenant hardware\. The host tenancy is not supported for Spot Instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)