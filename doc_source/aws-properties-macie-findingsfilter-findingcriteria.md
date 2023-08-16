# AWS::Macie::FindingsFilter FindingCriteria<a name="aws-properties-macie-findingsfilter-findingcriteria"></a>

Specifies, as a map, one or more property\-based conditions for a findings filter\. A *findings filter*, also referred to as a *filter rule*, is a set of custom criteria that specifies which findings to include or exclude from the results of a query for findings\. You can also configure a findings filter to suppress \(automatically archive\) findings that match the filter's criteria\. For more information, see [Filtering findings](https://docs.aws.amazon.com/macie/latest/user/findings-filter-overview.html) in the *Amazon Macie User Guide*\.

## Syntax<a name="aws-properties-macie-findingsfilter-findingcriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-macie-findingsfilter-findingcriteria-syntax.json"></a>

```
{
  "[Criterion](#cfn-macie-findingsfilter-findingcriteria-criterion)" : {Key: Value, ...}
}
```

### YAML<a name="aws-properties-macie-findingsfilter-findingcriteria-syntax.yaml"></a>

```
  [Criterion](#cfn-macie-findingsfilter-findingcriteria-criterion): 
    Key: Value
```

## Properties<a name="aws-properties-macie-findingsfilter-findingcriteria-properties"></a>

`Criterion`  <a name="cfn-macie-findingsfilter-findingcriteria-criterion"></a>
Specifies a condition that defines the property, operator, and one or more values to use to filter the results\.  
*Required*: No  
*Type*: Map of [CriterionAdditionalProperties](aws-properties-macie-findingsfilter-criterionadditionalproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)