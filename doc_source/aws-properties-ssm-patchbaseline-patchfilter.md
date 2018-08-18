# AWS Systems Manager PatchBaseline PatchFilter<a name="aws-properties-ssm-patchbaseline-patchfilter"></a>

<a name="aws-properties-ssm-patchbaseline-patchfilter-description"></a>The `PatchFilter` property type defines a patch filter for an AWS Systems Manager patch baseline\.

<a name="aws-properties-ssm-patchbaseline-patchfilter-inheritance"></a> The `PatchFilters` property of the [Systems Manager PatchBaseline PatchFilterGroup](aws-properties-ssm-patchbaseline-patchfiltergroup.md) property type contains a list of `PatchFilter` property types\. 

## Syntax<a name="aws-properties-ssm-patchbaseline-patchfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-patchfilter-syntax.json"></a>

```
{
  "[Key](#cfn-ssm-patchbaseline-patchfilter-key)" : String,
  "[Values](#cfn-ssm-patchbaseline-patchfilter-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-patchfilter-syntax.yaml"></a>

```
[Key](#cfn-ssm-patchbaseline-patchfilter-key): String
[Values](#cfn-ssm-patchbaseline-patchfilter-values): 
  - String
```

## Properties<a name="aws-properties-ssm-patchbaseline-patchfilter-properties"></a>

`Key`  <a name="cfn-ssm-patchbaseline-patchfilter-key"></a>
The key for the filter\. For information about valid keys, see [PatchFilter](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_PatchFilter.html) in the *AWS Systems Manager API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Values`  <a name="cfn-ssm-patchbaseline-patchfilter-values"></a>
The values for the filter key\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 