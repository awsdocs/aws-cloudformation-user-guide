# Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications Placement<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement"></a>

`Placement` is a property of the [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that defines the placement group for the Spot instances\.

## Syntax<a name="w3ab2c21c14d642b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname): String
```

## Properties<a name="w3ab2c21c14d642b7"></a>

`AvailabilityZone`  
The Availability Zone \(AZ\) of the placement group\.  
*Required: *No  
*Type*: String

`GroupName`  
The name of the placement group \(for cluster instances\)\.  
*Required: *No  
*Type*: String