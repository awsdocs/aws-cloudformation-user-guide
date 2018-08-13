# AWS CloudFormation Interface ParameterGroup<a name="aws-properties-cloudformation-interface-parametergroup"></a>

`ParameterGroup` is a property of the [AWS::CloudFormation::Interface](aws-resource-cloudformation-interface.md) resource that defines a parameter group and the parameters to include in the group\.

## Syntax<a name="w3ab2c21c14d231b5"></a>

### JSON<a name="aws-properties-cloudformation-interface-parametergroup-syntax.json"></a>

```
{
  "[Label](#cfn-cloudformation-interface-parametergroups-label)" : Label,
  "[Parameters](#cfn-cloudformation-interface-parametergroups-parameters)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudformation-interface-parametergroup-syntax.yaml"></a>

```
[Label](#cfn-cloudformation-interface-parametergroups-label): Label
[Parameters](#cfn-cloudformation-interface-parametergroups-parameters):
  - String
```

## Properties<a name="w3ab2c21c14d231b7"></a>

`Label`  <a name="cfn-cloudformation-interface-parametergroups-label"></a>
A name for the parameter group\.  
*Required*: No  
*Type*: [AWS CloudFormation Interface Label](aws-properties-cloudformation-interface-label.md)

`Parameters`  <a name="cfn-cloudformation-interface-parametergroups-parameters"></a>
A list of case\-sensitive parameter logical IDs to include in the group\. Parameters must already be defined in the `Parameters` section of the template\. A parameter can be included in only one parameter group\.  
The console lists the parameters that you don't associate with a parameter group in alphabetical order in the `Other parameters` group\.  
*Required*: No  
*Type*: List of String values