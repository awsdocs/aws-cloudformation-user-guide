# GuardDuty Filter FindingCriteria<a name="aws-properties-guardduty-filter-findingcriteria"></a>

<a name="aws-properties-guardduty-filter-findingcriteria-description"></a>The `FindingCriteria` property type specifies the attributes to be used in the filter and the conditions to be applied to the selected attributes for filtering through your GuardDuty findings\.

<a name="aws-properties-guardduty-filter-findingcriteria-inheritance"></a> `FindingCriteria` is a property of the [AWS::GuardDuty::Filter](aws-resource-guardduty-filter.md) resource\.

## Syntax<a name="aws-properties-guardduty-filter-findingcriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-filter-findingcriteria-syntax.json"></a>

```
{
  "[Criterion](#cfn-guardduty-filter-findingcriteria-criterion)" : Json,
  "[ItemType](#cfn-guardduty-filter-findingcriteria-itemtype)" : [*Condition*](aws-properties-guardduty-filter-condition.md)
}
```

### YAML<a name="aws-properties-guardduty-filter-findingcriteria-syntax.yaml"></a>

```
[Criterion](#cfn-guardduty-filter-findingcriteria-criterion): Json
[ItemType](#cfn-guardduty-filter-findingcriteria-itemtype): [*Condition*](aws-properties-guardduty-filter-condition.md)
```

## Properties<a name="aws-properties-guardduty-filter-findingcriteria-properties"></a>

`Criterion`  <a name="cfn-guardduty-filter-findingcriteria-criterion"></a>
Specifies the finding attributes \(for example, region, type, severity, etc\.\) that you want to include in the finding criteria for a filter\.   
 *Required*: No  
 *Type*: Json  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ItemType`  <a name="cfn-guardduty-filter-findingcriteria-itemtype"></a>
Specifies the condition to be applied to a single field when filtering through findings\.  
 *Required*: No  
 *Type*: [GuardDuty Filter Condition](aws-properties-guardduty-filter-condition.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 