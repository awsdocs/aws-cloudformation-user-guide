# AWS::EC2::EC2Fleet CapacityRebalance<a name="aws-properties-ec2-ec2fleet-capacityrebalance"></a>

The Spot Instance replacement strategy to use when Amazon EC2 emits a rebalance notification signal that your Spot Instance is at an elevated risk of being interrupted\. For more information, see [Capacity rebalancing](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet-capacity-rebalance.html) in the *Amazon EC2 User Guide*\.

## Syntax<a name="aws-properties-ec2-ec2fleet-capacityrebalance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-capacityrebalance-syntax.json"></a>

```
{
  "[ReplacementStrategy](#cfn-ec2-ec2fleet-capacityrebalance-replacementstrategy)" : String,
  "[TerminationDelay](#cfn-ec2-ec2fleet-capacityrebalance-terminationdelay)" : Integer
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-capacityrebalance-syntax.yaml"></a>

```
  [ReplacementStrategy](#cfn-ec2-ec2fleet-capacityrebalance-replacementstrategy): String
  [TerminationDelay](#cfn-ec2-ec2fleet-capacityrebalance-terminationdelay): Integer
```

## Properties<a name="aws-properties-ec2-ec2fleet-capacityrebalance-properties"></a>

`ReplacementStrategy`  <a name="cfn-ec2-ec2fleet-capacityrebalance-replacementstrategy"></a>
The replacement strategy to use\. Only available for fleets of type `maintain`\.  
 `launch` \- EC2 Fleet launches a replacement Spot Instance when a rebalance notification is emitted for an existing Spot Instance in the fleet\. EC2 Fleet does not terminate the instances that receive a rebalance notification\. You can terminate the old instances, or you can leave them running\. You are charged for all instances while they are running\.   
 `launch-before-terminate` \- EC2 Fleet launches a replacement Spot Instance when a rebalance notification is emitted for an existing Spot Instance in the fleet, and then, after a delay that you specify \(in `TerminationDelay`\), terminates the instances that received a rebalance notification\.  
*Required*: No  
*Type*: String  
*Allowed values*: `launch | launch-before-terminate`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TerminationDelay`  <a name="cfn-ec2-ec2fleet-capacityrebalance-terminationdelay"></a>
The amount of time \(in seconds\) that Amazon EC2 waits before terminating the old Spot Instance after launching a new replacement Spot Instance\.  
Required when `ReplacementStrategy` is set to `launch-before-terminate`\.  
Not valid when `ReplacementStrategy` is set to `launch`\.  
Valid values: Minimum value of `120` seconds\. Maximum value of `7200` seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)