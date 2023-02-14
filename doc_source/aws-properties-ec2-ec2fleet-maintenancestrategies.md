# AWS::EC2::EC2Fleet MaintenanceStrategies<a name="aws-properties-ec2-ec2fleet-maintenancestrategies"></a>

The strategies for managing your Spot Instances that are at an elevated risk of being interrupted\.

## Syntax<a name="aws-properties-ec2-ec2fleet-maintenancestrategies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-maintenancestrategies-syntax.json"></a>

```
{
  "[CapacityRebalance](#cfn-ec2-ec2fleet-maintenancestrategies-capacityrebalance)" : CapacityRebalance
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-maintenancestrategies-syntax.yaml"></a>

```
  [CapacityRebalance](#cfn-ec2-ec2fleet-maintenancestrategies-capacityrebalance): 
    CapacityRebalance
```

## Properties<a name="aws-properties-ec2-ec2fleet-maintenancestrategies-properties"></a>

`CapacityRebalance`  <a name="cfn-ec2-ec2fleet-maintenancestrategies-capacityrebalance"></a>
The strategy to use when Amazon EC2 emits a signal that your Spot Instance is at an elevated risk of being interrupted\.  
*Required*: No  
*Type*: [CapacityRebalance](aws-properties-ec2-ec2fleet-capacityrebalance.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)