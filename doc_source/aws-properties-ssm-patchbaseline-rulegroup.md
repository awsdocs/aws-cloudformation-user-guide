# AWS Systems Manager PatchBaseline RuleGroup<a name="aws-properties-ssm-patchbaseline-rulegroup"></a>

<a name="aws-properties-ssm-patchbaseline-rulegroup-description"></a>The `RuleGroup` property type specifies a set of rules that define the approval rules for a AWS Systems Manager patch baseline\.

<a name="aws-properties-ssm-patchbaseline-rulegroup-inheritance"></a> `RuleGroup` is the property type for the `ApprovalRules` property of the [AWS::SSM::PatchBaseline](aws-resource-ssm-patchbaseline.md) resource\. 

## Syntax<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax.json"></a>

```
{
  "[PatchRules](#cfn-ssm-patchbaseline-rulegroup-patchrules)" : [ [*Rule*](aws-properties-ssm-patchbaseline-rule.md), ... ]
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax.yaml"></a>

```
[PatchRules](#cfn-ssm-patchbaseline-rulegroup-patchrules): 
  - [*Rule*](aws-properties-ssm-patchbaseline-rule.md)
```

## Properties<a name="aws-properties-ssm-patchbaseline-rulegroup-properties"></a>

`PatchRules`  <a name="cfn-ssm-patchbaseline-rulegroup-patchrules"></a>
The rules that make up the rule group\.  
 *Required*: No  
 *Type*: List of [Systems Manager PatchBaseline Rule](aws-properties-ssm-patchbaseline-rule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 