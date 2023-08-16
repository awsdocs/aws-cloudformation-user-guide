# AWS::CustomerProfiles::CalculatedAttributeDefinition Range<a name="aws-properties-customerprofiles-calculatedattributedefinition-range"></a>

The relative time period over which data is included in the aggregation\.

## Syntax<a name="aws-properties-customerprofiles-calculatedattributedefinition-range-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-calculatedattributedefinition-range-syntax.json"></a>

```
{
  "[Unit](#cfn-customerprofiles-calculatedattributedefinition-range-unit)" : String,
  "[Value](#cfn-customerprofiles-calculatedattributedefinition-range-value)" : Integer
}
```

### YAML<a name="aws-properties-customerprofiles-calculatedattributedefinition-range-syntax.yaml"></a>

```
  [Unit](#cfn-customerprofiles-calculatedattributedefinition-range-unit): String
  [Value](#cfn-customerprofiles-calculatedattributedefinition-range-value): Integer
```

## Properties<a name="aws-properties-customerprofiles-calculatedattributedefinition-range-properties"></a>

`Unit`  <a name="cfn-customerprofiles-calculatedattributedefinition-range-unit"></a>
The unit of time\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-customerprofiles-calculatedattributedefinition-range-value"></a>
The amount of time of the specified unit\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)