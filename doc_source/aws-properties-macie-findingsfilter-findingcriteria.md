# AWS::Macie::FindingsFilter FindingCriteria<a name="aws-properties-macie-findingsfilter-findingcriteria"></a>

Specifies, as a map, one or more property\-based conditions that filter the results of a query for findings\.

## Syntax<a name="aws-properties-macie-findingsfilter-findingcriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-macie-findingsfilter-findingcriteria-syntax.json"></a>

```
{
  "[Criterion](#cfn-macie-findingsfilter-findingcriteria-criterion)" : Criterion
}
```

### YAML<a name="aws-properties-macie-findingsfilter-findingcriteria-syntax.yaml"></a>

```
  [Criterion](#cfn-macie-findingsfilter-findingcriteria-criterion): 
    Criterion
```

## Properties<a name="aws-properties-macie-findingsfilter-findingcriteria-properties"></a>

`Criterion`  <a name="cfn-macie-findingsfilter-findingcriteria-criterion"></a>
Specifies a condition that defines the property, operator, and value to use to filter the results\.  
*Required*: No  
*Type*: [Criterion](aws-properties-macie-findingsfilter-criterion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)