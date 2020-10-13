# AWS::EC2::EC2Fleet SpotOptionsRequest<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest"></a>

Specifies the configuration of Spot Instances for an EC2 Fleet\.

 `SpotOptionsRequest` is a property of the [ AWS::EC2::EC2Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-ec2fleet.html) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-ec2-ec2fleet-spotoptionsrequest-allocationstrategy)" : String,
  "[InstanceInterruptionBehavior](#cfn-ec2-ec2fleet-spotoptionsrequest-instanceinterruptionbehavior)" : String,
  "[InstancePoolsToUseCount](#cfn-ec2-ec2fleet-spotoptionsrequest-instancepoolstousecount)" : Integer,
  "[MaxTotalPrice](#cfn-ec2-ec2fleet-spotoptionsrequest-maxtotalprice)" : String,
  "[MinTargetCapacity](#cfn-ec2-ec2fleet-spotoptionsrequest-mintargetcapacity)" : Integer,
  "[SingleAvailabilityZone](#cfn-ec2-ec2fleet-spotoptionsrequest-singleavailabilityzone)" : Boolean,
  "[SingleInstanceType](#cfn-ec2-ec2fleet-spotoptionsrequest-singleinstancetype)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-syntax.yaml"></a>

```
  [AllocationStrategy](#cfn-ec2-ec2fleet-spotoptionsrequest-allocationstrategy): String
  [InstanceInterruptionBehavior](#cfn-ec2-ec2fleet-spotoptionsrequest-instanceinterruptionbehavior): String
  [InstancePoolsToUseCount](#cfn-ec2-ec2fleet-spotoptionsrequest-instancepoolstousecount): Integer
  [MaxTotalPrice](#cfn-ec2-ec2fleet-spotoptionsrequest-maxtotalprice): String
  [MinTargetCapacity](#cfn-ec2-ec2fleet-spotoptionsrequest-mintargetcapacity): Integer
  [SingleAvailabilityZone](#cfn-ec2-ec2fleet-spotoptionsrequest-singleavailabilityzone): Boolean
  [SingleInstanceType](#cfn-ec2-ec2fleet-spotoptionsrequest-singleinstancetype): Boolean
```

## Properties<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-properties"></a>

`AllocationStrategy`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-allocationstrategy"></a>
Indicates how to allocate the target Spot Instance capacity across the Spot Instance pools specified by the EC2 Fleet\.  
If the allocation strategy is `lowestPrice`, EC2 Fleet launches instances from the Spot Instance pools with the lowest price\. This is the default allocation strategy\.  
If the allocation strategy is `diversified`, EC2 Fleet launches instances from all the Spot Instance pools that you specify\.  
If the allocation strategy is `capacityOptimized`, EC2 Fleet launches instances from Spot Instance pools that are optimally chosen based on the available Spot Instance capacity\.  
*Allowed Values*: `lowestPrice` \| `diversified` \| `capacityOptimized`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceInterruptionBehavior`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-instanceinterruptionbehavior"></a>
The behavior when a Spot Instance is interrupted\. The default is `terminate`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `hibernate | stop | terminate`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstancePoolsToUseCount`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-instancepoolstousecount"></a>
The number of Spot pools across which to allocate your target Spot capacity\. Valid only when Spot **AllocationStrategy** is set to `lowest-price`\. EC2 Fleet selects the cheapest Spot pools and evenly allocates your target Spot capacity across the number of Spot pools that you specify\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxTotalPrice`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-maxtotalprice"></a>
The maximum amount per hour for Spot Instances that you're willing to pay\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinTargetCapacity`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-mintargetcapacity"></a>
The minimum target capacity for Spot Instances in the fleet\. If the minimum target capacity is not reached, the fleet launches no instances\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SingleAvailabilityZone`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-singleavailabilityzone"></a>
Indicates that the fleet launches all Spot Instances into a single Availability Zone\. Supported only for fleets of type `instant`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SingleInstanceType`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-singleinstancetype"></a>
Indicates that the fleet uses a single instance type to launch all Spot Instances in the fleet\. Supported only for fleets of type `instant`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest--seealso"></a>
+  [ SpotOptionsRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotOptionsRequest.html) in the *Amazon EC2 API Reference*