# Amazon Elastic Compute Cloud SpotFleet Placement<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement"></a>

`Placement` is a property of the [Amazon Elastic Compute Cloud SpotFleet LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that defines the placement group for the Spot instances\.

## Syntax<a name="w3ab2c21c14d814b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone)" : String,
  "[GroupName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-syntax.yaml"></a>

```
[AvailabilityZone](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone): String
[GroupName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname): String
```

## Properties<a name="w3ab2c21c14d814b7"></a>

`AvailabilityZone`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-availabilityzone"></a>
The Availability Zone \(AZ\) of the placement group\.  
*Required*: No  
*Type*: String

`GroupName`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement-groupname"></a>
The name of the placement group \(for cluster instances\)\.  
*Required*: No  
*Type*: String