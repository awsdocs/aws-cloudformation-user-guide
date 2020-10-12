# AWS::CloudFormation::StackSet StackInstances<a name="aws-properties-cloudformation-stackset-stackinstances"></a>

Stack instances in some specific accounts and Regions\.

## Syntax<a name="aws-properties-cloudformation-stackset-stackinstances-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-stackset-stackinstances-syntax.json"></a>

```
{
  "[DeploymentTargets](#cfn-cloudformation-stackset-stackinstances-deploymenttargets)" : DeploymentTargets,
  "[ParameterOverrides](#cfn-cloudformation-stackset-stackinstances-parameteroverrides)" : [ Parameter, ... ],
  "[Regions](#cfn-cloudformation-stackset-stackinstances-regions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudformation-stackset-stackinstances-syntax.yaml"></a>

```
  [DeploymentTargets](#cfn-cloudformation-stackset-stackinstances-deploymenttargets): 
    DeploymentTargets
  [ParameterOverrides](#cfn-cloudformation-stackset-stackinstances-parameteroverrides): 
    - Parameter
  [Regions](#cfn-cloudformation-stackset-stackinstances-regions): 
    - String
```

## Properties<a name="aws-properties-cloudformation-stackset-stackinstances-properties"></a>

`DeploymentTargets`  <a name="cfn-cloudformation-stackset-stackinstances-deploymenttargets"></a>
The AWS `OrganizationalUnitIds` or `Accounts` for which to create stack instances in the specified Regions\.  
*Required*: Yes  
*Type*: [DeploymentTargets](aws-properties-cloudformation-stackset-deploymenttargets.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterOverrides`  <a name="cfn-cloudformation-stackset-stackinstances-parameteroverrides"></a>
A list of stack set parameters whose values you want to override in the selected stack instances\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-cloudformation-stackset-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regions`  <a name="cfn-cloudformation-stackset-stackinstances-regions"></a>
The names of one or more Regions where you want to create stack instances using the specified AWS account\(s\)\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)