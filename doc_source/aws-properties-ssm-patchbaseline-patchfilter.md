# AWS::SSM::PatchBaseline PatchFilter<a name="aws-properties-ssm-patchbaseline-patchfilter"></a>

The `PatchFilter` property type defines a patch filter for an AWS Systems Manager patch baseline\.

The `PatchFilters` property of the [PatchFilterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-patchbaseline-patchfiltergroup.html) property type contains a list of `PatchFilter` property types\.

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
The key for the filter\.  
For information about valid keys, see [PatchFilter](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_PatchFilter.html) in the *AWS Systems Manager API Reference*\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `CLASSIFICATION | MSRC_SEVERITY | PATCH_ID | PATCH_SET | PRIORITY | PRODUCT | PRODUCT_FAMILY | SECTION | SEVERITY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-ssm-patchbaseline-patchfilter-values"></a>
The value for the filter key\.  
For information about valid values for each key based on operating system type, see [PatchFilter](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_PatchFilter.html) in the *AWS Systems Manager API Reference*\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
