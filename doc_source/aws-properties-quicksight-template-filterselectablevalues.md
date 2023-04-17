# AWS::QuickSight::Template FilterSelectableValues<a name="aws-properties-quicksight-template-filterselectablevalues"></a>

A list of selectable values that are used in a control\.

## Syntax<a name="aws-properties-quicksight-template-filterselectablevalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filterselectablevalues-syntax.json"></a>

```
{
  "[Values](#cfn-quicksight-template-filterselectablevalues-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-filterselectablevalues-syntax.yaml"></a>

```
  [Values](#cfn-quicksight-template-filterselectablevalues-values): 
    - String
```

## Properties<a name="aws-properties-quicksight-template-filterselectablevalues-properties"></a>

`Values`  <a name="cfn-quicksight-template-filterselectablevalues-values"></a>
The values that are used in the `FilterSelectableValues`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)