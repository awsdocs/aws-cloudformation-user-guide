# AWS::MWAA::Environment NetworkConfiguration<a name="aws-properties-mwaa-environment-networkconfiguration"></a>

The VPC networking components used to secure and enable network traffic between the AWS resources for your environment\. To learn more, see [About networking on Amazon MWAA](https://docs.aws.amazon.com/mwaa/latest/userguide/networking-about.html)\.

## Syntax<a name="aws-properties-mwaa-environment-networkconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-networkconfiguration-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-mwaa-environment-networkconfiguration-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-mwaa-environment-networkconfiguration-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-mwaa-environment-networkconfiguration-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-mwaa-environment-networkconfiguration-securitygroupids): 
    - String
  [SubnetIds](#cfn-mwaa-environment-networkconfiguration-subnetids): 
    - String
```

## Properties<a name="aws-properties-mwaa-environment-networkconfiguration-properties"></a>

`SecurityGroupIds`  <a name="cfn-mwaa-environment-networkconfiguration-securitygroupids"></a>
A list of one or more security group IDs\. Accepts up to 5 security group IDs\. A security group must be attached to the same VPC as the subnets\. To learn more, see [Security in your VPC on Amazon MWAA](https://docs.aws.amazon.com/mwaa/latest/userguide/vpc-security.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-mwaa-environment-networkconfiguration-subnetids"></a>
A list of subnet IDs\. **Required** to create an environment\. Must be private subnets in two different availability zones\. A subnet must be attached to the same VPC as the security group\. To learn more, see [About networking on Amazon MWAA](https://docs.aws.amazon.com/mwaa/latest/userguide/networking-about.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)