# AWS::EC2::SpotFleet SpotMaintenanceStrategies<a name="aws-properties-ec2-spotfleet-spotmaintenancestrategies"></a>

The strategies for managing your Spot Instances that are at an elevated risk of being interrupted\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotmaintenancestrategies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotmaintenancestrategies-syntax.json"></a>

```
{
  "[CapacityRebalance](#cfn-ec2-spotfleet-spotmaintenancestrategies-capacityrebalance)" : SpotCapacityRebalance
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotmaintenancestrategies-syntax.yaml"></a>

```
  [CapacityRebalance](#cfn-ec2-spotfleet-spotmaintenancestrategies-capacityrebalance): 
    SpotCapacityRebalance
```

## Properties<a name="aws-properties-ec2-spotfleet-spotmaintenancestrategies-properties"></a>

`CapacityRebalance`  <a name="cfn-ec2-spotfleet-spotmaintenancestrategies-capacityrebalance"></a>
The Spot Instance replacement strategy to use when Amazon EC2 emits a signal that your Spot Instance is at an elevated risk of being interrupted\. For more information, see [Capacity rebalancing](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet-capacity-rebalance.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: [SpotCapacityRebalance](aws-properties-ec2-spotfleet-spotcapacityrebalance.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)