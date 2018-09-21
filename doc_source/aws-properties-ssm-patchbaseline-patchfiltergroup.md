# AWS Systems Manager PatchBaseline PatchFilterGroup<a name="aws-properties-ssm-patchbaseline-patchfiltergroup"></a>

<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-description"></a>The `PatchFilterGroup` property type specifies a set of patch filters for an AWS Systems Manager patch baseline, typically used for approval rules for a Systems Manager patch baseline\.

<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-inheritance"></a> `PatchFilterGroup` is the property type for the `GlobalFilters` property of the [AWS::SSM::PatchBaseline](aws-resource-ssm-patchbaseline.md) resource and the `PatchFilterGroup` property of the [Systems Manager PatchBaseline Rule](aws-properties-ssm-patchbaseline-rule.md) property type\. 

## Syntax<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-syntax.json"></a>

```
{
  "[PatchFilters](#cfn-ssm-patchbaseline-patchfiltergroup-patchfilters)" : [ [*PatchFilter*](aws-properties-ssm-patchbaseline-patchfilter.md), ... ]
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-syntax.yaml"></a>

```
[PatchFilters](#cfn-ssm-patchbaseline-patchfiltergroup-patchfilters): 
  - [*PatchFilter*](aws-properties-ssm-patchbaseline-patchfilter.md)
```

## Properties<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-properties"></a>

`PatchFilters`  <a name="cfn-ssm-patchbaseline-patchfiltergroup-patchfilters"></a>
The set of patch filters that make up the group\.  
 *Required*: No  
 *Type*: List of [Systems Manager PatchBaseline PatchFilter](aws-properties-ssm-patchbaseline-patchfilter.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 