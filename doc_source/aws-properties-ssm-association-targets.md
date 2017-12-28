# Amazon EC2 Systems Manager Association Targets<a name="aws-properties-ssm-association-targets"></a>

`Targets` is a property of the [AWS::SSM::Association](aws-resource-ssm-association.md) resource that specifies the targets for an Amazon EC2 Systems Manager \(SSM\) document\.

## Syntax<a name="aws-properties-ssm-association-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-association-targets-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-targets-key)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-targets-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-association-targets-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-targets-key): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-targets-values):
  - String
```

## Properties<a name="w3ab2c21c14e1578b7"></a>

`Key`  
The name of the criteria that EC2 instances must meet\. For valid keys, see the [Target](http://docs.aws.amazon.com/ssm/latest/APIReference/API_Target.html) data type in the *Amazon EC2 Systems Manager API Reference*\.  
*Required: *Yes  
*Type*: String

`Values`  
The value of the criteria\. SSM runs targeted commands on EC2 instances that match the criteria\. For more information, see the [Target](http://docs.aws.amazon.com/ssm/latest/APIReference/API_Target.html) data type in the *Amazon EC2 Systems Manager API Reference*\.  
*Required: *Yes  
*Type*: List of String values