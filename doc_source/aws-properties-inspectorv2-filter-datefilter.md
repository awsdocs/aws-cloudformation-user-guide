# AWS::InspectorV2::Filter DateFilter<a name="aws-properties-inspectorv2-filter-datefilter"></a>

Contains details on the time range used to filter findings\.

## Syntax<a name="aws-properties-inspectorv2-filter-datefilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-inspectorv2-filter-datefilter-syntax.json"></a>

```
{
  "[EndInclusive](#cfn-inspectorv2-filter-datefilter-endinclusive)" : Integer,
  "[StartInclusive](#cfn-inspectorv2-filter-datefilter-startinclusive)" : Integer
}
```

### YAML<a name="aws-properties-inspectorv2-filter-datefilter-syntax.yaml"></a>

```
  [EndInclusive](#cfn-inspectorv2-filter-datefilter-endinclusive): Integer
  [StartInclusive](#cfn-inspectorv2-filter-datefilter-startinclusive): Integer
```

## Properties<a name="aws-properties-inspectorv2-filter-datefilter-properties"></a>

`EndInclusive`  <a name="cfn-inspectorv2-filter-datefilter-endinclusive"></a>
A timestamp representing the end of the time period filtered on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartInclusive`  <a name="cfn-inspectorv2-filter-datefilter-startinclusive"></a>
A timestamp representing the start of the time period filtered on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)