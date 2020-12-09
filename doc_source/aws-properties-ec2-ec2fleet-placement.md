# AWS::EC2::EC2Fleet Placement<a name="aws-properties-ec2-ec2fleet-placement"></a>

Describes the placement of an instance\.

## Syntax<a name="aws-properties-ec2-ec2fleet-placement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-placement-syntax.json"></a>

```
{
  "[Affinity](#cfn-ec2-ec2fleet-placement-affinity)" : String,
  "[AvailabilityZone](#cfn-ec2-ec2fleet-placement-availabilityzone)" : String,
  "[GroupName](#cfn-ec2-ec2fleet-placement-groupname)" : String,
  "[HostId](#cfn-ec2-ec2fleet-placement-hostid)" : String,
  "[HostResourceGroupArn](#cfn-ec2-ec2fleet-placement-hostresourcegrouparn)" : String,
  "[PartitionNumber](#cfn-ec2-ec2fleet-placement-partitionnumber)" : Integer,
  "[SpreadDomain](#cfn-ec2-ec2fleet-placement-spreaddomain)" : String,
  "[Tenancy](#cfn-ec2-ec2fleet-placement-tenancy)" : String
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-placement-syntax.yaml"></a>

```
  [Affinity](#cfn-ec2-ec2fleet-placement-affinity): String
  [AvailabilityZone](#cfn-ec2-ec2fleet-placement-availabilityzone): String
  [GroupName](#cfn-ec2-ec2fleet-placement-groupname): String
  [HostId](#cfn-ec2-ec2fleet-placement-hostid): String
  [HostResourceGroupArn](#cfn-ec2-ec2fleet-placement-hostresourcegrouparn): String
  [PartitionNumber](#cfn-ec2-ec2fleet-placement-partitionnumber): Integer
  [SpreadDomain](#cfn-ec2-ec2fleet-placement-spreaddomain): String
  [Tenancy](#cfn-ec2-ec2fleet-placement-tenancy): String
```

## Properties<a name="aws-properties-ec2-ec2fleet-placement-properties"></a>

`Affinity`  <a name="cfn-ec2-ec2fleet-placement-affinity"></a>
The affinity setting for the instance on the Dedicated Host\. This parameter is not supported for the [ImportInstance](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportInstance.html) command\.  
This parameter is not supported by [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AvailabilityZone`  <a name="cfn-ec2-ec2fleet-placement-availabilityzone"></a>
The Availability Zone of the instance\.  
If not specified, an Availability Zone will be automatically chosen for you based on the load balancing criteria for the Region\.  
This parameter is not supported by [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupName`  <a name="cfn-ec2-ec2fleet-placement-groupname"></a>
The name of the placement group the instance is in\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostId`  <a name="cfn-ec2-ec2fleet-placement-hostid"></a>
The ID of the Dedicated Host on which the instance resides\. This parameter is not supported for the [ImportInstance](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportInstance.html) command\.  
This parameter is not supported by [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostResourceGroupArn`  <a name="cfn-ec2-ec2fleet-placement-hostresourcegrouparn"></a>
The ARN of the host resource group in which to launch the instances\. If you specify a host resource group ARN, omit the **Tenancy** parameter or set it to `host`\.  
This parameter is not supported by [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PartitionNumber`  <a name="cfn-ec2-ec2fleet-placement-partitionnumber"></a>
The number of the partition the instance is in\. Valid only if the placement group strategy is set to `partition`\.  
This parameter is not supported by [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpreadDomain`  <a name="cfn-ec2-ec2fleet-placement-spreaddomain"></a>
Reserved for future use\.  
This parameter is not supported by [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tenancy`  <a name="cfn-ec2-ec2fleet-placement-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of `dedicated` runs on single\-tenant hardware\. The `host` tenancy is not supported for the [ImportInstance](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportInstance.html) command\.  
This parameter is not supported by [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `dedicated | default | host`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)