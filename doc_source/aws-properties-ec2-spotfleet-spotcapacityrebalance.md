# AWS::EC2::SpotFleet SpotCapacityRebalance<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance"></a>

The Spot Instance replacement strategy to use when Amazon EC2 emits a signal that your Spot Instance is at an elevated risk of being interrupted\. For more information, see [Capacity rebalancing](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet-capacity-rebalance.html) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-syntax.json"></a>

```
{
  "[ReplacementStrategy](#cfn-ec2-spotfleet-spotcapacityrebalance-replacementstrategy)" : String,
  "[TerminationDelay](#cfn-ec2-spotfleet-spotcapacityrebalance-terminationdelay)" : Integer
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-syntax.yaml"></a>

```
  [ReplacementStrategy](#cfn-ec2-spotfleet-spotcapacityrebalance-replacementstrategy): String
  [TerminationDelay](#cfn-ec2-spotfleet-spotcapacityrebalance-terminationdelay): Integer
```

## Properties<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-properties"></a>

`ReplacementStrategy`  <a name="cfn-ec2-spotfleet-spotcapacityrebalance-replacementstrategy"></a>
The replacement strategy to use\. Only available for fleets of type `maintain`\.  
 `launch` \- Spot Fleet launches a new replacement Spot Instance when a rebalance notification is emitted for an existing Spot Instance in the fleet\. Spot Fleet does not terminate the instances that receive a rebalance notification\. You can terminate the old instances, or you can leave them running\. You are charged for all instances while they are running\.   
 `launch-before-terminate` \- Spot Fleet launches a new replacement Spot Instance when a rebalance notification is emitted for an existing Spot Instance in the fleet, and then, after a delay that you specify \(in `TerminationDelay`\), terminates the instances that received a rebalance notification\.  
*Required*: No  
*Type*: String  
*Allowed values*: `launch | launch-before-terminate`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TerminationDelay`  <a name="cfn-ec2-spotfleet-spotcapacityrebalance-terminationdelay"></a>
The amount of time \(in seconds\) that Amazon EC2 waits before terminating the old Spot Instance after launching a new replacement Spot Instance\.  
Required when `ReplacementStrategy` is set to `launch-before-terminate`\.  
Not valid when `ReplacementStrategy` is set to `launch`\.  
Valid values: Minimum value of `120` seconds\. Maximum value of `7200` seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)