# GuardDuty Filter Condition<a name="aws-properties-guardduty-filter-condition"></a>

<a name="aws-properties-guardduty-filter-condition-description"></a>The `Condition` property type specifies the condition to be applied to a single field when filtering through GuardDuty findings\. 

<a name="aws-properties-guardduty-filter-condition-inheritance"></a> `Condition` is a property of the [GuardDuty Filter FindingCriteria](aws-properties-guardduty-filter-findingcriteria.md) property type\.

## Syntax<a name="aws-properties-guardduty-filter-condition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-filter-condition-syntax.json"></a>

```
{
  "[Lt](#cfn-guardduty-filter-condition-lt)" : Integer,
  "[Gte](#cfn-guardduty-filter-condition-gte)" : Integer,
  "[Neq](#cfn-guardduty-filter-condition-neq)" : [ String, ... ],
  "[Eq](#cfn-guardduty-filter-condition-eq)" : [ String, ... ],
  "[Lte](#cfn-guardduty-filter-condition-lte)" : Integer
}
```

### YAML<a name="aws-properties-guardduty-filter-condition-syntax.yaml"></a>

```
[Lt](#cfn-guardduty-filter-condition-lt): Integer
[Gte](#cfn-guardduty-filter-condition-gte): Integer
[Neq](#cfn-guardduty-filter-condition-neq): 
  - String
[Eq](#cfn-guardduty-filter-condition-eq): 
  - String
[Lte](#cfn-guardduty-filter-condition-lte): Integer
```

## Properties<a name="aws-properties-guardduty-filter-condition-properties"></a>

`Lt`  <a name="cfn-guardduty-filter-condition-lt"></a>
Represents the "less than" condition to be applied to a single field when filtering through findings\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Gte`  <a name="cfn-guardduty-filter-condition-gte"></a>
Represents the "greater than equal" condition to be applied to a single field when filtering through findings\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Neq`  <a name="cfn-guardduty-filter-condition-neq"></a>
Represents the "not equal to" condition to be applied to a single field when filtering through findings\.   
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Eq`  <a name="cfn-guardduty-filter-condition-eq"></a>
Represents the "equal to" condition to be applied to a single field when filtering through findings\.   
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Lte`  <a name="cfn-guardduty-filter-condition-lte"></a>
Represents the "less than equal" condition to be applied to a single field when filtering through findings\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 