# AWS::QuickSight::Dashboard PivotTablePaginatedReportOptions<a name="aws-properties-quicksight-dashboard-pivottablepaginatedreportoptions"></a>

The paginated report options for a pivot table visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottablepaginatedreportoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottablepaginatedreportoptions-syntax.json"></a>

```
{
  "[OverflowColumnHeaderVisibility](#cfn-quicksight-dashboard-pivottablepaginatedreportoptions-overflowcolumnheadervisibility)" : String,
  "[VerticalOverflowVisibility](#cfn-quicksight-dashboard-pivottablepaginatedreportoptions-verticaloverflowvisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottablepaginatedreportoptions-syntax.yaml"></a>

```
  [OverflowColumnHeaderVisibility](#cfn-quicksight-dashboard-pivottablepaginatedreportoptions-overflowcolumnheadervisibility): String
  [VerticalOverflowVisibility](#cfn-quicksight-dashboard-pivottablepaginatedreportoptions-verticaloverflowvisibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottablepaginatedreportoptions-properties"></a>

`OverflowColumnHeaderVisibility`  <a name="cfn-quicksight-dashboard-pivottablepaginatedreportoptions-overflowcolumnheadervisibility"></a>
The visibility of the repeating header rows on each page\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerticalOverflowVisibility`  <a name="cfn-quicksight-dashboard-pivottablepaginatedreportoptions-verticaloverflowvisibility"></a>
The visibility of the printing table overflow across pages\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)