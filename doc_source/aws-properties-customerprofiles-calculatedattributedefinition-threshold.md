# AWS::CustomerProfiles::CalculatedAttributeDefinition Threshold<a name="aws-properties-customerprofiles-calculatedattributedefinition-threshold"></a>

The threshold for the calculated attribute\.

## Syntax<a name="aws-properties-customerprofiles-calculatedattributedefinition-threshold-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-calculatedattributedefinition-threshold-syntax.json"></a>

```
{
  "[Operator](#cfn-customerprofiles-calculatedattributedefinition-threshold-operator)" : String,
  "[Value](#cfn-customerprofiles-calculatedattributedefinition-threshold-value)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-calculatedattributedefinition-threshold-syntax.yaml"></a>

```
  [Operator](#cfn-customerprofiles-calculatedattributedefinition-threshold-operator): String
  [Value](#cfn-customerprofiles-calculatedattributedefinition-threshold-value): String
```

## Properties<a name="aws-properties-customerprofiles-calculatedattributedefinition-threshold-properties"></a>

`Operator`  <a name="cfn-customerprofiles-calculatedattributedefinition-threshold-operator"></a>
The operator of the threshold\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-customerprofiles-calculatedattributedefinition-threshold-value"></a>
The value of the threshold\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)