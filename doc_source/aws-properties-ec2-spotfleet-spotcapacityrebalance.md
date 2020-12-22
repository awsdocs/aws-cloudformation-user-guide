# AWS::EC2::SpotFleet SpotCapacityRebalance<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance"></a>

The Spot Instance replacement strategy to use when Amazon EC2 emits a signal that your Spot Instance is at an elevated risk of being interrupted\. For more information, see [Capacity rebalancing](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet-configuration-strategies.html#spot-fleet-capacity-rebalance) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-syntax.json"></a>

```
{
  "[ReplacementStrategy](#cfn-ec2-spotfleet-spotcapacityrebalance-replacementstrategy)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-syntax.yaml"></a>

```
  [ReplacementStrategy](#cfn-ec2-spotfleet-spotcapacityrebalance-replacementstrategy): String
```

## Properties<a name="aws-properties-ec2-spotfleet-spotcapacityrebalance-properties"></a>

`ReplacementStrategy`  <a name="cfn-ec2-spotfleet-spotcapacityrebalance-replacementstrategy"></a>
The replacement strategy to use\. Only available for fleets of type `maintain`\. You must specify a value, otherwise you get an error\.  
To allow Spot Fleet to launch a replacement Spot Instance when an instance rebalance notification is emitted for a Spot Instance in the fleet, specify `launch`\.  
When a replacement instance is launched, the instance marked for rebalance is not automatically terminated\. You can terminate it, or you can leave it running\. You are charged for all instances while they are running\.
*Required*: No  
*Type*: String  
*Allowed values*: `launch`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)