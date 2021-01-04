# AWS::MWAA::Environment NetworkConfiguration<a name="aws-properties-mwaa-environment-networkconfiguration"></a>

The Network Configuration to update of your Amazon MWAA environment\.

## Syntax<a name="aws-properties-mwaa-environment-networkconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-networkconfiguration-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-mwaa-environment-networkconfiguration-securitygroupids)" : SecurityGroupList,
  "[SubnetIds](#cfn-mwaa-environment-networkconfiguration-subnetids)" : SubnetList
}
```

### YAML<a name="aws-properties-mwaa-environment-networkconfiguration-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-mwaa-environment-networkconfiguration-securitygroupids): 
    SecurityGroupList
  [SubnetIds](#cfn-mwaa-environment-networkconfiguration-subnetids): 
    SubnetList
```

## Properties<a name="aws-properties-mwaa-environment-networkconfiguration-properties"></a>

`SecurityGroupIds`  <a name="cfn-mwaa-environment-networkconfiguration-securitygroupids"></a>
A JSON list of 1 or more security group IDs, by name, that are in the same VPC as the subnets\.  
*Required*: No  
*Type*: [SecurityGroupList](aws-properties-mwaa-environment-securitygrouplist.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-mwaa-environment-networkconfiguration-subnetids"></a>
Provide a JSON list of 2 subnet IDs by name\. These must be private subnets, in the same VPC, in two different availability zones\.  
*Required*: No  
*Type*: [SubnetList](aws-properties-mwaa-environment-subnetlist.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)