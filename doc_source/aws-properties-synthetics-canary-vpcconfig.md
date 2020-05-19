# AWS::Synthetics::Canary VPCConfig<a name="aws-properties-synthetics-canary-vpcconfig"></a>

If this canary is to test an endpoint in a VPC, this structure contains information about the subnet and security groups of the VPC endpoint\. For more information, see [ Running a Canary in a VPC](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_VPC.html)\.

## Syntax<a name="aws-properties-synthetics-canary-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-synthetics-canary-vpcconfig-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-synthetics-canary-vpcconfig-subnetids)" : [ String, ... ],
  "[VpcId](#cfn-synthetics-canary-vpcconfig-vpcid)" : String
}
```

### YAML<a name="aws-properties-synthetics-canary-vpcconfig-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-synthetics-canary-vpcconfig-securitygroupids): 
    - String
  [SubnetIds](#cfn-synthetics-canary-vpcconfig-subnetids): 
    - String
  [VpcId](#cfn-synthetics-canary-vpcconfig-vpcid): String
```

## Properties<a name="aws-properties-synthetics-canary-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-synthetics-canary-vpcconfig-securitygroupids"></a>
The IDs of the security groups for this canary\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-synthetics-canary-vpcconfig-subnetids"></a>
The IDs of the subnets where this canary is to run\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-synthetics-canary-vpcconfig-vpcid"></a>
The ID of the VPC where this canary is to run\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)