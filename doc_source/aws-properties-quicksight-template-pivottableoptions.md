# AWS::QuickSight::Template PivotTableOptions<a name="aws-properties-quicksight-template-pivottableoptions"></a>

The table options for a pivot table visual\.

## Syntax<a name="aws-properties-quicksight-template-pivottableoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivottableoptions-syntax.json"></a>

```
{
  "[CellStyle](#cfn-quicksight-template-pivottableoptions-cellstyle)" : TableCellStyle,
  "[CollapsedRowDimensionsVisibility](#cfn-quicksight-template-pivottableoptions-collapsedrowdimensionsvisibility)" : String,
  "[ColumnHeaderStyle](#cfn-quicksight-template-pivottableoptions-columnheaderstyle)" : TableCellStyle,
  "[ColumnNamesVisibility](#cfn-quicksight-template-pivottableoptions-columnnamesvisibility)" : String,
  "[DefaultCellWidth](#cfn-quicksight-template-pivottableoptions-defaultcellwidth)" : String,
  "[MetricPlacement](#cfn-quicksight-template-pivottableoptions-metricplacement)" : String,
  "[RowAlternateColorOptions](#cfn-quicksight-template-pivottableoptions-rowalternatecoloroptions)" : RowAlternateColorOptions,
  "[RowFieldNamesStyle](#cfn-quicksight-template-pivottableoptions-rowfieldnamesstyle)" : TableCellStyle,
  "[RowHeaderStyle](#cfn-quicksight-template-pivottableoptions-rowheaderstyle)" : TableCellStyle,
  "[RowsLabelOptions](#cfn-quicksight-template-pivottableoptions-rowslabeloptions)" : PivotTableRowsLabelOptions,
  "[RowsLayout](#cfn-quicksight-template-pivottableoptions-rowslayout)" : String,
  "[SingleMetricVisibility](#cfn-quicksight-template-pivottableoptions-singlemetricvisibility)" : String,
  "[ToggleButtonsVisibility](#cfn-quicksight-template-pivottableoptions-togglebuttonsvisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-pivottableoptions-syntax.yaml"></a>

```
  [CellStyle](#cfn-quicksight-template-pivottableoptions-cellstyle): 
    TableCellStyle
  [CollapsedRowDimensionsVisibility](#cfn-quicksight-template-pivottableoptions-collapsedrowdimensionsvisibility): String
  [ColumnHeaderStyle](#cfn-quicksight-template-pivottableoptions-columnheaderstyle): 
    TableCellStyle
  [ColumnNamesVisibility](#cfn-quicksight-template-pivottableoptions-columnnamesvisibility): String
  [DefaultCellWidth](#cfn-quicksight-template-pivottableoptions-defaultcellwidth): String
  [MetricPlacement](#cfn-quicksight-template-pivottableoptions-metricplacement): String
  [RowAlternateColorOptions](#cfn-quicksight-template-pivottableoptions-rowalternatecoloroptions): 
    RowAlternateColorOptions
  [RowFieldNamesStyle](#cfn-quicksight-template-pivottableoptions-rowfieldnamesstyle): 
    TableCellStyle
  [RowHeaderStyle](#cfn-quicksight-template-pivottableoptions-rowheaderstyle): 
    TableCellStyle
  [RowsLabelOptions](#cfn-quicksight-template-pivottableoptions-rowslabeloptions): 
    PivotTableRowsLabelOptions
  [RowsLayout](#cfn-quicksight-template-pivottableoptions-rowslayout): String
  [SingleMetricVisibility](#cfn-quicksight-template-pivottableoptions-singlemetricvisibility): String
  [ToggleButtonsVisibility](#cfn-quicksight-template-pivottableoptions-togglebuttonsvisibility): String
```

## Properties<a name="aws-properties-quicksight-template-pivottableoptions-properties"></a>

`CellStyle`  <a name="cfn-quicksight-template-pivottableoptions-cellstyle"></a>
The table cell style of cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CollapsedRowDimensionsVisibility`  <a name="cfn-quicksight-template-pivottableoptions-collapsedrowdimensionsvisibility"></a>
The visibility setting of a pivot table's collapsed row dimension fields\. If the value of this structure is `HIDDEN`, all collapsed columns in a pivot table are automatically hidden\. The default value is `VISIBLE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHeaderStyle`  <a name="cfn-quicksight-template-pivottableoptions-columnheaderstyle"></a>
The table cell style of the column header\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnNamesVisibility`  <a name="cfn-quicksight-template-pivottableoptions-columnnamesvisibility"></a>
The visibility of the column names\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultCellWidth`  <a name="cfn-quicksight-template-pivottableoptions-defaultcellwidth"></a>
The default cell width of the pivot table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricPlacement`  <a name="cfn-quicksight-template-pivottableoptions-metricplacement"></a>
The metric placement \(row, column\) options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COLUMN | ROW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowAlternateColorOptions`  <a name="cfn-quicksight-template-pivottableoptions-rowalternatecoloroptions"></a>
The row alternate color options \(widget status, row alternate colors\)\.  
*Required*: No  
*Type*: [RowAlternateColorOptions](aws-properties-quicksight-template-rowalternatecoloroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowFieldNamesStyle`  <a name="cfn-quicksight-template-pivottableoptions-rowfieldnamesstyle"></a>
The table cell style of row field names\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowHeaderStyle`  <a name="cfn-quicksight-template-pivottableoptions-rowheaderstyle"></a>
The table cell style of the row headers\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowsLabelOptions`  <a name="cfn-quicksight-template-pivottableoptions-rowslabeloptions"></a>
The options for the label that is located above the row headers\. This option is only applicable when `RowsLayout` is set to `HIERARCHY`\.  
*Required*: No  
*Type*: [PivotTableRowsLabelOptions](aws-properties-quicksight-template-pivottablerowslabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowsLayout`  <a name="cfn-quicksight-template-pivottableoptions-rowslayout"></a>
The layout for the row dimension headers of a pivot table\. Choose one of the following options\.  
+  `TABULAR`: \(Default\) Each row field is displayed in a separate column\.
+  `HIERARCHY`: All row fields are displayed in a single column\. Indentation is used to differentiate row headers of different fields\.
*Required*: No  
*Type*: String  
*Allowed values*: `HIERARCHY | TABULAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleMetricVisibility`  <a name="cfn-quicksight-template-pivottableoptions-singlemetricvisibility"></a>
The visibility of the single metric options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ToggleButtonsVisibility`  <a name="cfn-quicksight-template-pivottableoptions-togglebuttonsvisibility"></a>
Determines the visibility of the pivot table\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)