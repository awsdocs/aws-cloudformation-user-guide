# AWS::QuickSight::Dashboard PivotTableOptions<a name="aws-properties-quicksight-dashboard-pivottableoptions"></a>

The table options for a pivot table visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottableoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottableoptions-syntax.json"></a>

```
{
  "[CellStyle](#cfn-quicksight-dashboard-pivottableoptions-cellstyle)" : TableCellStyle,
  "[ColumnHeaderStyle](#cfn-quicksight-dashboard-pivottableoptions-columnheaderstyle)" : TableCellStyle,
  "[ColumnNamesVisibility](#cfn-quicksight-dashboard-pivottableoptions-columnnamesvisibility)" : String,
  "[MetricPlacement](#cfn-quicksight-dashboard-pivottableoptions-metricplacement)" : String,
  "[RowAlternateColorOptions](#cfn-quicksight-dashboard-pivottableoptions-rowalternatecoloroptions)" : RowAlternateColorOptions,
  "[RowFieldNamesStyle](#cfn-quicksight-dashboard-pivottableoptions-rowfieldnamesstyle)" : TableCellStyle,
  "[RowHeaderStyle](#cfn-quicksight-dashboard-pivottableoptions-rowheaderstyle)" : TableCellStyle,
  "[SingleMetricVisibility](#cfn-quicksight-dashboard-pivottableoptions-singlemetricvisibility)" : String,
  "[ToggleButtonsVisibility](#cfn-quicksight-dashboard-pivottableoptions-togglebuttonsvisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottableoptions-syntax.yaml"></a>

```
  [CellStyle](#cfn-quicksight-dashboard-pivottableoptions-cellstyle): 
    TableCellStyle
  [ColumnHeaderStyle](#cfn-quicksight-dashboard-pivottableoptions-columnheaderstyle): 
    TableCellStyle
  [ColumnNamesVisibility](#cfn-quicksight-dashboard-pivottableoptions-columnnamesvisibility): String
  [MetricPlacement](#cfn-quicksight-dashboard-pivottableoptions-metricplacement): String
  [RowAlternateColorOptions](#cfn-quicksight-dashboard-pivottableoptions-rowalternatecoloroptions): 
    RowAlternateColorOptions
  [RowFieldNamesStyle](#cfn-quicksight-dashboard-pivottableoptions-rowfieldnamesstyle): 
    TableCellStyle
  [RowHeaderStyle](#cfn-quicksight-dashboard-pivottableoptions-rowheaderstyle): 
    TableCellStyle
  [SingleMetricVisibility](#cfn-quicksight-dashboard-pivottableoptions-singlemetricvisibility): String
  [ToggleButtonsVisibility](#cfn-quicksight-dashboard-pivottableoptions-togglebuttonsvisibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottableoptions-properties"></a>

`CellStyle`  <a name="cfn-quicksight-dashboard-pivottableoptions-cellstyle"></a>
The table cell style of cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHeaderStyle`  <a name="cfn-quicksight-dashboard-pivottableoptions-columnheaderstyle"></a>
The table cell style of the column header\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnNamesVisibility`  <a name="cfn-quicksight-dashboard-pivottableoptions-columnnamesvisibility"></a>
The visibility of the column names\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricPlacement`  <a name="cfn-quicksight-dashboard-pivottableoptions-metricplacement"></a>
The metric placement \(row, column\) options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COLUMN | ROW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowAlternateColorOptions`  <a name="cfn-quicksight-dashboard-pivottableoptions-rowalternatecoloroptions"></a>
The row alternate color options \(widget status, row alternate colors\)\.  
*Required*: No  
*Type*: [RowAlternateColorOptions](aws-properties-quicksight-dashboard-rowalternatecoloroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowFieldNamesStyle`  <a name="cfn-quicksight-dashboard-pivottableoptions-rowfieldnamesstyle"></a>
The table cell style of row field names\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowHeaderStyle`  <a name="cfn-quicksight-dashboard-pivottableoptions-rowheaderstyle"></a>
The table cell style of the row headers\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleMetricVisibility`  <a name="cfn-quicksight-dashboard-pivottableoptions-singlemetricvisibility"></a>
The visibility of the single metric options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToggleButtonsVisibility`  <a name="cfn-quicksight-dashboard-pivottableoptions-togglebuttonsvisibility"></a>
Determines the visibility of the pivot table\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)