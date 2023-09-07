# AWS::QuickSight::Analysis PivotTableOptions<a name="aws-properties-quicksight-analysis-pivottableoptions"></a>

The table options for a pivot table visual\.

## Syntax<a name="aws-properties-quicksight-analysis-pivottableoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-pivottableoptions-syntax.json"></a>

```
{
  "[CellStyle](#cfn-quicksight-analysis-pivottableoptions-cellstyle)" : TableCellStyle,
  "[CollapsedRowDimensionsVisibility](#cfn-quicksight-analysis-pivottableoptions-collapsedrowdimensionsvisibility)" : String,
  "[ColumnHeaderStyle](#cfn-quicksight-analysis-pivottableoptions-columnheaderstyle)" : TableCellStyle,
  "[ColumnNamesVisibility](#cfn-quicksight-analysis-pivottableoptions-columnnamesvisibility)" : String,
  "[DefaultCellWidth](#cfn-quicksight-analysis-pivottableoptions-defaultcellwidth)" : String,
  "[MetricPlacement](#cfn-quicksight-analysis-pivottableoptions-metricplacement)" : String,
  "[RowAlternateColorOptions](#cfn-quicksight-analysis-pivottableoptions-rowalternatecoloroptions)" : RowAlternateColorOptions,
  "[RowFieldNamesStyle](#cfn-quicksight-analysis-pivottableoptions-rowfieldnamesstyle)" : TableCellStyle,
  "[RowHeaderStyle](#cfn-quicksight-analysis-pivottableoptions-rowheaderstyle)" : TableCellStyle,
  "[RowsLabelOptions](#cfn-quicksight-analysis-pivottableoptions-rowslabeloptions)" : PivotTableRowsLabelOptions,
  "[RowsLayout](#cfn-quicksight-analysis-pivottableoptions-rowslayout)" : String,
  "[SingleMetricVisibility](#cfn-quicksight-analysis-pivottableoptions-singlemetricvisibility)" : String,
  "[ToggleButtonsVisibility](#cfn-quicksight-analysis-pivottableoptions-togglebuttonsvisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-pivottableoptions-syntax.yaml"></a>

```
  [CellStyle](#cfn-quicksight-analysis-pivottableoptions-cellstyle): 
    TableCellStyle
  [CollapsedRowDimensionsVisibility](#cfn-quicksight-analysis-pivottableoptions-collapsedrowdimensionsvisibility): String
  [ColumnHeaderStyle](#cfn-quicksight-analysis-pivottableoptions-columnheaderstyle): 
    TableCellStyle
  [ColumnNamesVisibility](#cfn-quicksight-analysis-pivottableoptions-columnnamesvisibility): String
  [DefaultCellWidth](#cfn-quicksight-analysis-pivottableoptions-defaultcellwidth): String
  [MetricPlacement](#cfn-quicksight-analysis-pivottableoptions-metricplacement): String
  [RowAlternateColorOptions](#cfn-quicksight-analysis-pivottableoptions-rowalternatecoloroptions): 
    RowAlternateColorOptions
  [RowFieldNamesStyle](#cfn-quicksight-analysis-pivottableoptions-rowfieldnamesstyle): 
    TableCellStyle
  [RowHeaderStyle](#cfn-quicksight-analysis-pivottableoptions-rowheaderstyle): 
    TableCellStyle
  [RowsLabelOptions](#cfn-quicksight-analysis-pivottableoptions-rowslabeloptions): 
    PivotTableRowsLabelOptions
  [RowsLayout](#cfn-quicksight-analysis-pivottableoptions-rowslayout): String
  [SingleMetricVisibility](#cfn-quicksight-analysis-pivottableoptions-singlemetricvisibility): String
  [ToggleButtonsVisibility](#cfn-quicksight-analysis-pivottableoptions-togglebuttonsvisibility): String
```

## Properties<a name="aws-properties-quicksight-analysis-pivottableoptions-properties"></a>

`CellStyle`  <a name="cfn-quicksight-analysis-pivottableoptions-cellstyle"></a>
The table cell style of cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CollapsedRowDimensionsVisibility`  <a name="cfn-quicksight-analysis-pivottableoptions-collapsedrowdimensionsvisibility"></a>
The visibility setting of a pivot table's collapsed row dimension fields\. If the value of this structure is `HIDDEN`, all collapsed columns in a pivot table are automatically hidden\. The default value is `VISIBLE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHeaderStyle`  <a name="cfn-quicksight-analysis-pivottableoptions-columnheaderstyle"></a>
The table cell style of the column header\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnNamesVisibility`  <a name="cfn-quicksight-analysis-pivottableoptions-columnnamesvisibility"></a>
The visibility of the column names\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultCellWidth`  <a name="cfn-quicksight-analysis-pivottableoptions-defaultcellwidth"></a>
The default cell width of the pivot table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricPlacement`  <a name="cfn-quicksight-analysis-pivottableoptions-metricplacement"></a>
The metric placement \(row, column\) options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COLUMN | ROW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowAlternateColorOptions`  <a name="cfn-quicksight-analysis-pivottableoptions-rowalternatecoloroptions"></a>
The row alternate color options \(widget status, row alternate colors\)\.  
*Required*: No  
*Type*: [RowAlternateColorOptions](aws-properties-quicksight-analysis-rowalternatecoloroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowFieldNamesStyle`  <a name="cfn-quicksight-analysis-pivottableoptions-rowfieldnamesstyle"></a>
The table cell style of row field names\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowHeaderStyle`  <a name="cfn-quicksight-analysis-pivottableoptions-rowheaderstyle"></a>
The table cell style of the row headers\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowsLabelOptions`  <a name="cfn-quicksight-analysis-pivottableoptions-rowslabeloptions"></a>
The options for the label that is located above the row headers\. This option is only applicable when `RowsLayout` is set to `HIERARCHY`\.  
*Required*: No  
*Type*: [PivotTableRowsLabelOptions](aws-properties-quicksight-analysis-pivottablerowslabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowsLayout`  <a name="cfn-quicksight-analysis-pivottableoptions-rowslayout"></a>
The layout for the row dimension headers of a pivot table\. Choose one of the following options\.  
+  `TABULAR`: \(Default\) Each row field is displayed in a separate column\.
+  `HIERARCHY`: All row fields are displayed in a single column\. Indentation is used to differentiate row headers of different fields\.
*Required*: No  
*Type*: String  
*Allowed values*: `HIERARCHY | TABULAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleMetricVisibility`  <a name="cfn-quicksight-analysis-pivottableoptions-singlemetricvisibility"></a>
The visibility of the single metric options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToggleButtonsVisibility`  <a name="cfn-quicksight-analysis-pivottableoptions-togglebuttonsvisibility"></a>
Determines the visibility of the pivot table\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)