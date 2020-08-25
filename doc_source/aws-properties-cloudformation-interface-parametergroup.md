# AWS CloudFormation interface ParameterGroup<a name="aws-properties-cloudformation-interface-parametergroup"></a>

`ParameterGroup` is a property of the [AWS::CloudFormation::Interface](aws-resource-cloudformation-interface.md) resource that defines a parameter group and the parameters to include in the group\.

## Syntax<a name="w6640ab1c19c15c15c27c23b5"></a>

### JSON<a name="aws-properties-cloudformation-interface-parametergroup-syntax.json"></a>

```
{
  "" : Label,
  "" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudformation-interface-parametergroup-syntax.yaml"></a>

```
: Label
:
  - String
```

## Properties<a name="w6640ab1c19c15c15c27c23b7"></a>

`Label`  <a name="cfn-cloudformation-interface-parametergroups-label"></a>
A name for the parameter group\.  
*Required*: No  
*Type*: [AWS CloudFormation interface label](aws-properties-cloudformation-interface-label.md)

`Parameters`  <a name="cfn-cloudformation-interface-parametergroups-parameters"></a>
A list of case\-sensitive parameter logical IDs to include in the group\. Parameters must already be defined in the `Parameters` section of the template\. A parameter can be included in only one parameter group\.  
The console lists the parameters that you don't associate with a parameter group in alphabetical order in the `Other parameters` group\.  
*Required*: No  
*Type*: List of String values