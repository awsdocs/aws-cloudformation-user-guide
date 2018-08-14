# AWS Systems Manager Association Targets<a name="aws-properties-ssm-association-targets"></a>

`Targets` is a property of the [AWS::SSM::Association](aws-resource-ssm-association.md) resource that specifies the targets for an SSM document in Systems Manager\.

## Syntax<a name="aws-properties-ssm-association-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-association-targets-syntax.json"></a>

```
{
  "[Key](#cfn-ssm-association-targets-key)" : String,
  "[Values](#cfn-ssm-association-targets-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-association-targets-syntax.yaml"></a>

```
[Key](#cfn-ssm-association-targets-key): String
[Values](#cfn-ssm-association-targets-values):
  - String
```

## Properties<a name="w3ab2c21c14e1938b7"></a>

`Key`  <a name="cfn-ssm-association-targets-key"></a>
The name of the criteria that EC2 instances must meet\. For valid keys, see the [Target](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_Target.html) data type in the *AWS Systems Manager API Reference*\.  
*Required*: Yes  
*Type*: String

`Values`  <a name="cfn-ssm-association-targets-values"></a>
The value of the criteria\. Systems Manager runs targeted commands on EC2 instances that match the criteria\. For more information, see the [Target](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_Target.html) data type in the *AWS Systems Manager API Reference*\.  
*Required*: Yes  
*Type*: List of String values