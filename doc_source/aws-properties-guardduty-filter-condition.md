# AWS::GuardDuty::Filter Condition<a name="aws-properties-guardduty-filter-condition"></a>

Specifies the condition to apply to a single field when filtering through GuardDuty findings\.

## Syntax<a name="aws-properties-guardduty-filter-condition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-filter-condition-syntax.json"></a>

```
{
  "[Eq](#cfn-guardduty-filter-condition-eq)" : [ String, ... ],
  "[Gte](#cfn-guardduty-filter-condition-gte)" : Integer,
  "[Lt](#cfn-guardduty-filter-condition-lt)" : Integer,
  "[Lte](#cfn-guardduty-filter-condition-lte)" : Integer,
  "[Neq](#cfn-guardduty-filter-condition-neq)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-guardduty-filter-condition-syntax.yaml"></a>

```
  [Eq](#cfn-guardduty-filter-condition-eq): 
    - String
  [Gte](#cfn-guardduty-filter-condition-gte): Integer
  [Lt](#cfn-guardduty-filter-condition-lt): Integer
  [Lte](#cfn-guardduty-filter-condition-lte): Integer
  [Neq](#cfn-guardduty-filter-condition-neq): 
    - String
```

## Properties<a name="aws-properties-guardduty-filter-condition-properties"></a>

`Eq`  <a name="cfn-guardduty-filter-condition-eq"></a>
Represents the equal condition to apply to a single field when querying for findings\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Gte`  <a name="cfn-guardduty-filter-condition-gte"></a>
Represents the greater than or equal condition to apply to a single field when querying for findings\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lt`  <a name="cfn-guardduty-filter-condition-lt"></a>
Represents the less than condition to apply to a single field when querying for findings\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lte`  <a name="cfn-guardduty-filter-condition-lte"></a>
Represents the less than or equal condition to apply to a single field when querying for findings\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Neq`  <a name="cfn-guardduty-filter-condition-neq"></a>
Represents the not equal condition to apply to a single field when querying for findings\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)