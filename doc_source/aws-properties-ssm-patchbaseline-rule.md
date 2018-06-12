# AWS Systems Manager PatchBaseline Rule<a name="aws-properties-ssm-patchbaseline-rule"></a>

<a name="aws-properties-ssm-patchbaseline-rule-description"></a>The `Rule` property type specifies an approval rule for a Systems Manager patch baseline\.

<a name="aws-properties-ssm-patchbaseline-rule-inheritance"></a> The `PatchRules` property of the [Systems Manager PatchBaseline RuleGroup](aws-properties-ssm-patchbaseline-rulegroup.md) property type contains a list of `Rule` property types\. 

## Syntax<a name="aws-properties-ssm-patchbaseline-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-rule-syntax.json"></a>

```
{
  "[PatchFilterGroup](#cfn-ssm-patchbaseline-rule-patchfiltergroup)" : [*PatchFilterGroup*](aws-properties-ssm-patchbaseline-patchfiltergroup.md),
  "[ApproveAfterDays](#cfn-ssm-patchbaseline-rule-approveafterdays)" : Integer,
  "[ComplianceLevel](#cfn-ssm-patchbaseline-rule-compliancelevel)" : String
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-rule-syntax.yaml"></a>

```
[PatchFilterGroup](#cfn-ssm-patchbaseline-rule-patchfiltergroup): 
  [*PatchFilterGroup*](aws-properties-ssm-patchbaseline-patchfiltergroup.md)
[ApproveAfterDays](#cfn-ssm-patchbaseline-rule-approveafterdays): Integer
[ComplianceLevel](#cfn-ssm-patchbaseline-rule-compliancelevel): String
```

## Properties<a name="aws-properties-ssm-patchbaseline-rule-properties"></a>

`PatchFilterGroup`  <a name="cfn-ssm-patchbaseline-rule-patchfiltergroup"></a>
The patch filter group that defines the criteria for the rule\.  
 *Required*: No  
 *Type*: [Systems Manager PatchBaseline PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApproveAfterDays`  <a name="cfn-ssm-patchbaseline-rule-approveafterdays"></a>
The number of days after the release date of each patch matched by the rule that the patch is marked as approved in the patch baseline\. For example, a value of `7` means that patches are approved seven days after they are released\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ComplianceLevel`  <a name="cfn-ssm-patchbaseline-rule-compliancelevel"></a>
A compliance severity level for all approved patches in a patch baseline\. Valid compliance severity levels include the following: `Unspecified`, `Critical`, `High`, `Medium`, `Low`, and `Informational`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 