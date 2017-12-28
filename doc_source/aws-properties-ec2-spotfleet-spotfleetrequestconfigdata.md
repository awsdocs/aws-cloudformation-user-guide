# Amazon EC2 SpotFleet SpotFleetRequestConfigData<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata"></a>

`SpotFleetRequestConfigData` is a property of the [AWS::EC2::SpotFleet](aws-resource-ec2-spotfleet.md) resource that defines the configuration of a Spot fleet request\.

## Syntax<a name="w3ab2c21c14d609b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-allocationstrategy)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-excesscapacityterminationpolicy)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-iamfleetrole)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications)" : [ LaunchSpecifications, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-replaceunhealthyinstances)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-spotprice)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-targetcapacity)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-terminateinstanceswithexpiration)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-type)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validfrom)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validuntil)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-allocationstrategy): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-excesscapacityterminationpolicy): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-iamfleetrole): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications):
  - LaunchSpecifications
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-replaceunhealthyinstances): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-spotprice): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-targetcapacity): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-terminateinstanceswithexpiration): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-type): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validfrom): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-validuntil): String
```

## Properties<a name="w3ab2c21c14d609b7"></a>

`AllocationStrategy`  
Indicates how to allocate the target capacity across the Spot pools that you specified in the Spot fleet request\. For valid values, see [SpotFleetRequestConfigData](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotFleetRequestConfigData.html) in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`ExcessCapacityTerminationPolicy`  
Indicates whether running Spot instances are terminated if you decrease the target capacity of the Spot fleet request below the current size of the Spot fleet\. For valid values, see [SpotFleetRequestConfigData](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotFleetRequestConfigData.html) in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`IamFleetRole`  
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that grants the Spot fleet the ability to bid on, launch, and terminate instances on your behalf\. For more information, see [Spot Fleet Prerequisites](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet-requests.html#spot-fleet-prerequisites) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`LaunchSpecifications`  
The launch specifications for the Spot fleet request\.  
*Required: *Yes  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md)  
*Update requires*: Replacement

`ReplaceUnhealthyInstances`  
Indicates whether the Spot fleet should replace unhealthy instances\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`SpotPrice`  
The bid price per unit hour\. For more information, see [How Spot Fleet Works](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`TargetCapacity`  
The number of units to request for the spot fleet\. You can choose to set the target capacity as the number of instances or as a performance characteristic that is important to your application workload, such as vCPUs, memory, or I/O\. For more information, see [How Spot Fleet Works](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *Yes  
*Type*: Integer  
*Update requires*: No interruption

`TerminateInstancesWithExpiration`  
Indicates whether running Spot instances are terminated when the Spot fleet request expires\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`Type`  
The type of request, which indicates whether the fleet will only request the target capacity or also attempt to maintain it\. For more information, see [SpotFleetRequestConfigData](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotFleetRequestConfigData.html) in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`ValidFrom`  
The start date and time of the request, in UTC format \(*YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. By default, Amazon Elastic Compute Cloud \(Amazon EC2 \) starts fulfilling the request immediately\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`ValidUntil`  
The end date and time of the request, in UTC format \(*YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. After the end date and time, Amazon EC2 doesn't request new Spot instances or enable them to fulfill the request\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement