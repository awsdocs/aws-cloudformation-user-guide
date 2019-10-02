# AWS::SSM::PatchBaseline PatchFilterGroup<a name="aws-properties-ssm-patchbaseline-patchfiltergroup"></a>

The `PatchFilterGroup` property type specifies a set of patch filters for an AWS Systems Manager patch baseline, typically used for approval rules for a Systems Manager patch baseline\.

 `PatchFilterGroup` is the property type for the `GlobalFilters` property of the [AWS::SSM::PatchBaseline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-patchbaseline.html) resource and the `PatchFilterGroup` property of the [Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-patchbaseline-rule.html) property type\.

## Syntax<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-syntax.json"></a>

```
{
  "[PatchFilters](#cfn-ssm-patchbaseline-patchfiltergroup-patchfilters)" : [ [PatchFilter](aws-properties-ssm-patchbaseline-patchfilter.md), ... ]
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-syntax.yaml"></a>

```
  [PatchFilters](#cfn-ssm-patchbaseline-patchfiltergroup-patchfilters): 
    - [PatchFilter](aws-properties-ssm-patchbaseline-patchfilter.md)
```

## Properties<a name="aws-properties-ssm-patchbaseline-patchfiltergroup-properties"></a>

`PatchFilters`  <a name="cfn-ssm-patchbaseline-patchfiltergroup-patchfilters"></a>
The set of patch filters that make up the group\.  
*Required*: No  
*Type*: List of [PatchFilter](aws-properties-ssm-patchbaseline-patchfilter.md)  
*Maximum*: `4`  
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
