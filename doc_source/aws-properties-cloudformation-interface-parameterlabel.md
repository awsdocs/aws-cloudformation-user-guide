# AWS CloudFormation interface ParameterLabel<a name="aws-properties-cloudformation-interface-parameterlabel"></a>

`ParameterLabel` is a property of the [AWS::CloudFormation::Interface](aws-resource-cloudformation-interface.md) resource that specifies a friendly name or description for a parameter that the AWS CloudFormation console shows instead of the parameter's logical ID\.

## Syntax<a name="w6948ab1c28c15c15c27c27b5"></a>

### JSON<a name="aws-properties-cloudformation-interface-parameterlabel-syntax.json"></a>

```
{
  "" : Label
}
```

### YAML<a name="aws-properties-cloudformation-interface-parameterlabel-syntax.yaml"></a>

```
: Label
```

## Properties<a name="w6948ab1c28c15c15c27c27b7"></a>

`ParameterLogicalID`  <a name="cfn-cloudformation-interface-parameterlabel-parameterlogicalid"></a>
A label for a parameter\. The label defines a friendly name or description that the AWS CloudFormation console shows on the **Specify Parameters** page when a stack is created or updated\. The `ParameterLogicalID` key must be the case\-sensitive logical ID of a valid parameter that has been declared in the `Parameters` section of the template\.  
*Required*: No  
*Type*: [AWS CloudFormation interface label](aws-properties-cloudformation-interface-label.md)