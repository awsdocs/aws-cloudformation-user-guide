# AWS::DeviceFarm::TestGridProject VpcConfig<a name="aws-properties-devicefarm-testgridproject-vpcconfig"></a>

The VPC security groups and subnets attached to the `TestGrid` project\.

## Syntax<a name="aws-properties-devicefarm-testgridproject-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-devicefarm-testgridproject-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-devicefarm-testgridproject-vpcconfig-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-devicefarm-testgridproject-vpcconfig-subnetids)" : [ String, ... ],
  "[VpcId](#cfn-devicefarm-testgridproject-vpcconfig-vpcid)" : String
}
```

### YAML<a name="aws-properties-devicefarm-testgridproject-vpcconfig-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-devicefarm-testgridproject-vpcconfig-securitygroupids): 
    - String
  [SubnetIds](#cfn-devicefarm-testgridproject-vpcconfig-subnetids): 
    - String
  [VpcId](#cfn-devicefarm-testgridproject-vpcconfig-vpcid): String
```

## Properties<a name="aws-properties-devicefarm-testgridproject-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-devicefarm-testgridproject-vpcconfig-securitygroupids"></a>
A list of VPC security group IDs\.  
A security group allows inbound traffic from network interfaces \(and their associated instances\) that are assigned to the same security group\. See [Security groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) in the *Amazon Virtual Private Cloud user guide*\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-devicefarm-testgridproject-vpcconfig-subnetids"></a>
A list of VPC subnet IDs\.  
A subnet is a range of IP addresses in your VPC\. You can launch Amazon resources, such as EC2 instances, into a specific subnet\. When you create a subnet, you specify the IPv4 CIDR block for the subnet, which is a subset of the VPC CIDR block\. See [VPCs and subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) in the *Amazon Virtual Private Cloud user guide*\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-devicefarm-testgridproject-vpcconfig-vpcid"></a>
A list of VPC IDs\.  
Each VPC is given a unique ID upon creation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)