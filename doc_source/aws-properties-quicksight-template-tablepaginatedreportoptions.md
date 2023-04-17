# AWS::QuickSight::Template TablePaginatedReportOptions<a name="aws-properties-quicksight-template-tablepaginatedreportoptions"></a>

The paginated report options for a table visual\.

## Syntax<a name="aws-properties-quicksight-template-tablepaginatedreportoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tablepaginatedreportoptions-syntax.json"></a>

```
{
  "[OverflowColumnHeaderVisibility](#cfn-quicksight-template-tablepaginatedreportoptions-overflowcolumnheadervisibility)" : String,
  "[VerticalOverflowVisibility](#cfn-quicksight-template-tablepaginatedreportoptions-verticaloverflowvisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-tablepaginatedreportoptions-syntax.yaml"></a>

```
  [OverflowColumnHeaderVisibility](#cfn-quicksight-template-tablepaginatedreportoptions-overflowcolumnheadervisibility): String
  [VerticalOverflowVisibility](#cfn-quicksight-template-tablepaginatedreportoptions-verticaloverflowvisibility): String
```

## Properties<a name="aws-properties-quicksight-template-tablepaginatedreportoptions-properties"></a>

`OverflowColumnHeaderVisibility`  <a name="cfn-quicksight-template-tablepaginatedreportoptions-overflowcolumnheadervisibility"></a>
The visibility of repeating header rows on each page\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerticalOverflowVisibility`  <a name="cfn-quicksight-template-tablepaginatedreportoptions-verticaloverflowvisibility"></a>
The visibility of printing table overflow across pages\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)