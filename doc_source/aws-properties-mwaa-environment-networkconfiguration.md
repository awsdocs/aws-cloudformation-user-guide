# AWS::MWAA::Environment NetworkConfiguration<a name="aws-properties-mwaa-environment-networkconfiguration"></a>



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
  
*Required*: No  
*Type*: [SecurityGroupList](aws-properties-mwaa-environment-securitygrouplist.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-mwaa-environment-networkconfiguration-subnetids"></a>
  
*Required*: No  
*Type*: [SubnetList](aws-properties-mwaa-environment-subnetlist.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)