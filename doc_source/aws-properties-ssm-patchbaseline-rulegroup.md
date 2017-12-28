# Amazon EC2 Systems Manager PatchBaseline RuleGroup<a name="aws-properties-ssm-patchbaseline-rulegroup"></a>

<a name="aws-properties-ssm-patchbaseline-rulegroup-description"></a>The `RuleGroup` property type specifies a set of rules that define the approval rules for an Amazon EC2 Systems Manager patch baseline\.

<a name="aws-properties-ssm-patchbaseline-rulegroup-inheritance"></a> `RuleGroup` is the property type for the `ApprovalRules` property of the [AWS::SSM::PatchBaseline](aws-resource-ssm-patchbaseline.md) resource\. 

## Syntax<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-rulegroup-patchrules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-patchbaseline-rulegroup-patchrules): 
  - Rule
```

## Properties<a name="aws-properties-ssm-patchbaseline-rulegroup-properties"></a>

`PatchRules`  
The rules that make up the rule group\.  
 *Required*: No  
 *Type*: List of [SSM PatchBaseline Rule](aws-properties-ssm-patchbaseline-rule.md)  
 *Update requires*: No interruption 