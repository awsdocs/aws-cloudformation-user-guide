# AWS::QuickSight::Dashboard PivotFieldSortOptions<a name="aws-properties-quicksight-dashboard-pivotfieldsortoptions"></a>

The field sort options for a pivot table sort configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivotfieldsortoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivotfieldsortoptions-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-dashboard-pivotfieldsortoptions-fieldid)" : String,
  "[SortBy](#cfn-quicksight-dashboard-pivotfieldsortoptions-sortby)" : PivotTableSortBy
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivotfieldsortoptions-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-dashboard-pivotfieldsortoptions-fieldid): String
  [SortBy](#cfn-quicksight-dashboard-pivotfieldsortoptions-sortby): 
    PivotTableSortBy
```

## Properties<a name="aws-properties-quicksight-dashboard-pivotfieldsortoptions-properties"></a>

`FieldId`  <a name="cfn-quicksight-dashboard-pivotfieldsortoptions-fieldid"></a>
The field ID for the field sort options\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortBy`  <a name="cfn-quicksight-dashboard-pivotfieldsortoptions-sortby"></a>
The sort by field for the field sort options\.  
*Required*: Yes  
*Type*: [PivotTableSortBy](aws-properties-quicksight-dashboard-pivottablesortby.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)