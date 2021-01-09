# AWS::MWAA::Environment SubnetList<a name="aws-properties-mwaa-environment-subnetlist"></a>

Provide a JSON list of 2 subnet IDs by name\. These must be private subnets, in the same VPC, in two different availability zones\.

## Syntax<a name="aws-properties-mwaa-environment-subnetlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-subnetlist-syntax.json"></a>

```
{
  "[SubnetList](#cfn-mwaa-environment-subnetlist-subnetlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-mwaa-environment-subnetlist-syntax.yaml"></a>

```
  [SubnetList](#cfn-mwaa-environment-subnetlist-subnetlist): 
    - String
```

## Properties<a name="aws-properties-mwaa-environment-subnetlist-properties"></a>

`SubnetList`  <a name="cfn-mwaa-environment-subnetlist-subnetlist"></a>
The list of subnets\.  
*Required*: No  
*Type*: [List](#aws-properties-mwaa-environment-subnetlist) of [String](#aws-properties-mwaa-environment-subnetlist)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)