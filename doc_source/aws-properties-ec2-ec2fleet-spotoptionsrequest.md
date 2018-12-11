# Amazon EC2 EC2Fleet SpotOptionsRequest<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest"></a>

<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-description"></a>The `SpotOptionsRequest` property type specifies the configuration of Spot Instances for an EC2 Fleet\.

<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-inheritance"></a> `SpotOptionsRequest` is a property of the [AWS::EC2::EC2Fleet](aws-resource-ec2-ec2fleet.md) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-ec2-ec2fleet-spotoptionsrequest-allocationstrategy)" : String,
  "[InstanceInterruptionBehavior](#cfn-ec2-ec2fleet-spotoptionsrequest-instanceinterruptionbehavior)" : String,
  "[InstancePoolsToUseCount](#cfn-ec2-ec2fleet-spotoptionsrequest-instancepoolstousecount)" : Integer
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-syntax.yaml"></a>

```
[AllocationStrategy](#cfn-ec2-ec2fleet-spotoptionsrequest-allocationstrategy): String
[InstanceInterruptionBehavior](#cfn-ec2-ec2fleet-spotoptionsrequest-instanceinterruptionbehavior): String
[InstancePoolsToUseCount](#cfn-ec2-ec2fleet-spotoptionsrequest-instancepoolstousecount): Integer
```

## Properties<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-properties"></a>

`AllocationStrategy`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-allocationstrategy"></a>
Indicates how to allocate the target capacity across the Spot pools specified by the Spot Fleet request\. The default is `lowestPrice`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstanceInterruptionBehavior`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-instanceinterruptionbehavior"></a>
The behavior when a Spot Instance is interrupted\. The default is `terminate`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstancePoolsToUseCount`  <a name="cfn-ec2-ec2fleet-spotoptionsrequest-instancepoolstousecount"></a>
The number of Spot pools across which to allocate your target Spot capacity\. Valid only when Spot **AllocationStrategy** is set to `lowest-price`\. EC2 Fleet selects the cheapest Spot pools and evenly allocates your target Spot capacity across the number of Spot pools that you specify\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-ec2fleet-spotoptionsrequest-seealso"></a>
+ [SpotOptionsRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotOptionsRequest.html) in the *Amazon EC2 API Reference*