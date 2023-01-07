# AWS::SSM::PatchBaseline RuleGroup<a name="aws-properties-ssm-patchbaseline-rulegroup"></a>

The `RuleGroup` property type specifies a set of rules that define the approval rules for an AWS Systems Manager patch baseline\.

 `RuleGroup` is the property type for the `ApprovalRules` property of the [AWS::SSM::PatchBaseline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-patchbaseline.html) resource\. 

## Syntax<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax.json"></a>

```
{
  "[PatchRules](#cfn-ssm-patchbaseline-rulegroup-patchrules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-rulegroup-syntax.yaml"></a>

```
  [PatchRules](#cfn-ssm-patchbaseline-rulegroup-patchrules): 
    - Rule
```

## Properties<a name="aws-properties-ssm-patchbaseline-rulegroup-properties"></a>

`PatchRules`  <a name="cfn-ssm-patchbaseline-rulegroup-patchrules"></a>
The rules that make up the rule group\.  
*Required*: No  
*Type*: List of [Rule](aws-properties-ssm-patchbaseline-rule.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)