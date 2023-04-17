# AWS::QuickSight::Template PivotFieldSortOptions<a name="aws-properties-quicksight-template-pivotfieldsortoptions"></a>

The field sort options for a pivot table sort configuration\.

## Syntax<a name="aws-properties-quicksight-template-pivotfieldsortoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivotfieldsortoptions-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-template-pivotfieldsortoptions-fieldid)" : String,
  "[SortBy](#cfn-quicksight-template-pivotfieldsortoptions-sortby)" : PivotTableSortBy
}
```

### YAML<a name="aws-properties-quicksight-template-pivotfieldsortoptions-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-template-pivotfieldsortoptions-fieldid): String
  [SortBy](#cfn-quicksight-template-pivotfieldsortoptions-sortby): 
    PivotTableSortBy
```

## Properties<a name="aws-properties-quicksight-template-pivotfieldsortoptions-properties"></a>

`FieldId`  <a name="cfn-quicksight-template-pivotfieldsortoptions-fieldid"></a>
The field ID for the field sort options\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortBy`  <a name="cfn-quicksight-template-pivotfieldsortoptions-sortby"></a>
The sort by field for the field sort options\.  
*Required*: Yes  
*Type*: [PivotTableSortBy](aws-properties-quicksight-template-pivottablesortby.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)