# AWS::MWAA::Environment SecurityGroupList<a name="aws-properties-mwaa-environment-securitygrouplist"></a>

A list of security groups to use for the environment\.

## Syntax<a name="aws-properties-mwaa-environment-securitygrouplist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-securitygrouplist-syntax.json"></a>

```
{
  "[SecurityGroupList](#cfn-mwaa-environment-securitygrouplist-securitygrouplist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-mwaa-environment-securitygrouplist-syntax.yaml"></a>

```
  [SecurityGroupList](#cfn-mwaa-environment-securitygrouplist-securitygrouplist): 
    - String
```

## Properties<a name="aws-properties-mwaa-environment-securitygrouplist-properties"></a>

`SecurityGroupList`  <a name="cfn-mwaa-environment-securitygrouplist-securitygrouplist"></a>
A list of security groups\.  
*Required*: No  
*Type*: [List](#aws-properties-mwaa-environment-securitygrouplist) of [String](#aws-properties-mwaa-environment-securitygrouplist)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)