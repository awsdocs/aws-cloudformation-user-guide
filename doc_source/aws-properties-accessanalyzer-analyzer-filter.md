# AWS::AccessAnalyzer::Analyzer Filter<a name="aws-properties-accessanalyzer-analyzer-filter"></a>

The criteria that defines the rule\.

## Syntax<a name="aws-properties-accessanalyzer-analyzer-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-accessanalyzer-analyzer-filter-syntax.json"></a>

```
{
  "[Contains](#cfn-accessanalyzer-analyzer-filter-contains)" : [ String, ... ],
  "[Eq](#cfn-accessanalyzer-analyzer-filter-eq)" : [ String, ... ],
  "[Exists](#cfn-accessanalyzer-analyzer-filter-exists)" : Boolean,
  "[Neq](#cfn-accessanalyzer-analyzer-filter-neq)" : [ String, ... ],
  "[Property](#cfn-accessanalyzer-analyzer-filter-property)" : String
}
```

### YAML<a name="aws-properties-accessanalyzer-analyzer-filter-syntax.yaml"></a>

```
  [Contains](#cfn-accessanalyzer-analyzer-filter-contains): 
    - String
  [Eq](#cfn-accessanalyzer-analyzer-filter-eq): 
    - String
  [Exists](#cfn-accessanalyzer-analyzer-filter-exists): Boolean
  [Neq](#cfn-accessanalyzer-analyzer-filter-neq): 
    - String
  [Property](#cfn-accessanalyzer-analyzer-filter-property): String
```

## Properties<a name="aws-properties-accessanalyzer-analyzer-filter-properties"></a>

`Contains`  <a name="cfn-accessanalyzer-analyzer-filter-contains"></a>
A "contains" condition to match for the rule\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Eq`  <a name="cfn-accessanalyzer-analyzer-filter-eq"></a>
An "equals" condition to match for the rule\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Exists`  <a name="cfn-accessanalyzer-analyzer-filter-exists"></a>
An "exists" condition to match for the rule\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Neq`  <a name="cfn-accessanalyzer-analyzer-filter-neq"></a>
A "not equal" condition to match for the rule\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Property`  <a name="cfn-accessanalyzer-analyzer-filter-property"></a>
The property used to define the criteria in the filter for the rule\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)