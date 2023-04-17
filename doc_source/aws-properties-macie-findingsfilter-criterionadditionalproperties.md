# AWS::Macie::FindingsFilter CriterionAdditionalProperties<a name="aws-properties-macie-findingsfilter-criterionadditionalproperties"></a>

Specifies a condition that defines the property, operator, and one or more values to use in a findings filter\. A *findings filter*, also referred to as a *filter rule*, is a set of custom criteria that specifies which findings to include or exclude from the results of a query for findings\. You can also configure a findings filter to suppress \(automatically archive\) findings that match the filter's criteria\. For more information, see [Filtering findings](https://docs.aws.amazon.com/macie/latest/user/findings-filter-overview.html) in the *Amazon Macie User Guide*\.

## Syntax<a name="aws-properties-macie-findingsfilter-criterionadditionalproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-macie-findingsfilter-criterionadditionalproperties-syntax.json"></a>

```
{
  "[eq](#cfn-macie-findingsfilter-criterionadditionalproperties-eq)" : [ String, ... ],
  "[gt](#cfn-macie-findingsfilter-criterionadditionalproperties-gt)" : Integer,
  "[gte](#cfn-macie-findingsfilter-criterionadditionalproperties-gte)" : Integer,
  "[lt](#cfn-macie-findingsfilter-criterionadditionalproperties-lt)" : Integer,
  "[lte](#cfn-macie-findingsfilter-criterionadditionalproperties-lte)" : Integer,
  "[neq](#cfn-macie-findingsfilter-criterionadditionalproperties-neq)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-macie-findingsfilter-criterionadditionalproperties-syntax.yaml"></a>

```
  [eq](#cfn-macie-findingsfilter-criterionadditionalproperties-eq): 
    - String
  [gt](#cfn-macie-findingsfilter-criterionadditionalproperties-gt): Integer
  [gte](#cfn-macie-findingsfilter-criterionadditionalproperties-gte): Integer
  [lt](#cfn-macie-findingsfilter-criterionadditionalproperties-lt): Integer
  [lte](#cfn-macie-findingsfilter-criterionadditionalproperties-lte): Integer
  [neq](#cfn-macie-findingsfilter-criterionadditionalproperties-neq): 
    - String
```

## Properties<a name="aws-properties-macie-findingsfilter-criterionadditionalproperties-properties"></a>

`eq`  <a name="cfn-macie-findingsfilter-criterionadditionalproperties-eq"></a>
The value for the specified property matches \(equals\) the specified value\. If you specify multiple values, Amazon Macie uses OR logic to join the values\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`gt`  <a name="cfn-macie-findingsfilter-criterionadditionalproperties-gt"></a>
The value for the specified property is greater than the specified value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`gte`  <a name="cfn-macie-findingsfilter-criterionadditionalproperties-gte"></a>
The value for the specified property is greater than or equal to the specified value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`lt`  <a name="cfn-macie-findingsfilter-criterionadditionalproperties-lt"></a>
The value for the specified property is less than the specified value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`lte`  <a name="cfn-macie-findingsfilter-criterionadditionalproperties-lte"></a>
The value for the specified property is less than or equal to the specified value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`neq`  <a name="cfn-macie-findingsfilter-criterionadditionalproperties-neq"></a>
The value for the specified property doesn't match \(doesn't equal\) the specified value\. If you specify multiple values, Amazon Macie uses OR logic to join the values\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)