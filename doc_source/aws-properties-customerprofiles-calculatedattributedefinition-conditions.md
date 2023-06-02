# AWS::CustomerProfiles::CalculatedAttributeDefinition Conditions<a name="aws-properties-customerprofiles-calculatedattributedefinition-conditions"></a>

The conditions including range, object count, and threshold for the calculated attribute\.

## Syntax<a name="aws-properties-customerprofiles-calculatedattributedefinition-conditions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-calculatedattributedefinition-conditions-syntax.json"></a>

```
{
  "[ObjectCount](#cfn-customerprofiles-calculatedattributedefinition-conditions-objectcount)" : Integer,
  "[Range](#cfn-customerprofiles-calculatedattributedefinition-conditions-range)" : Range,
  "[Threshold](#cfn-customerprofiles-calculatedattributedefinition-conditions-threshold)" : Threshold
}
```

### YAML<a name="aws-properties-customerprofiles-calculatedattributedefinition-conditions-syntax.yaml"></a>

```
  [ObjectCount](#cfn-customerprofiles-calculatedattributedefinition-conditions-objectcount): Integer
  [Range](#cfn-customerprofiles-calculatedattributedefinition-conditions-range): 
    Range
  [Threshold](#cfn-customerprofiles-calculatedattributedefinition-conditions-threshold): 
    Threshold
```

## Properties<a name="aws-properties-customerprofiles-calculatedattributedefinition-conditions-properties"></a>

`ObjectCount`  <a name="cfn-customerprofiles-calculatedattributedefinition-conditions-objectcount"></a>
The number of profile objects used for the calculated attribute\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Range`  <a name="cfn-customerprofiles-calculatedattributedefinition-conditions-range"></a>
The relative time period over which data is included in the aggregation\.  
*Required*: No  
*Type*: [Range](aws-properties-customerprofiles-calculatedattributedefinition-range.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Threshold`  <a name="cfn-customerprofiles-calculatedattributedefinition-conditions-threshold"></a>
The threshold for the calculated attribute\.  
*Required*: No  
*Type*: [Threshold](aws-properties-customerprofiles-calculatedattributedefinition-threshold.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)