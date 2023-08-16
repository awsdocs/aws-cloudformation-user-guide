# AWS::QuickSight::Analysis TableConfiguration<a name="aws-properties-quicksight-analysis-tableconfiguration"></a>

The configuration for a `TableVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-tableconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tableconfiguration-syntax.json"></a>

```
{
  "[FieldOptions](#cfn-quicksight-analysis-tableconfiguration-fieldoptions)" : TableFieldOptions,
  "[FieldWells](#cfn-quicksight-analysis-tableconfiguration-fieldwells)" : TableFieldWells,
  "[PaginatedReportOptions](#cfn-quicksight-analysis-tableconfiguration-paginatedreportoptions)" : TablePaginatedReportOptions,
  "[SortConfiguration](#cfn-quicksight-analysis-tableconfiguration-sortconfiguration)" : TableSortConfiguration,
  "[TableInlineVisualizations](#cfn-quicksight-analysis-tableconfiguration-tableinlinevisualizations)" : [ TableInlineVisualization, ... ],
  "[TableOptions](#cfn-quicksight-analysis-tableconfiguration-tableoptions)" : TableOptions,
  "[TotalOptions](#cfn-quicksight-analysis-tableconfiguration-totaloptions)" : TotalOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-tableconfiguration-syntax.yaml"></a>

```
  [FieldOptions](#cfn-quicksight-analysis-tableconfiguration-fieldoptions): 
    TableFieldOptions
  [FieldWells](#cfn-quicksight-analysis-tableconfiguration-fieldwells): 
    TableFieldWells
  [PaginatedReportOptions](#cfn-quicksight-analysis-tableconfiguration-paginatedreportoptions): 
    TablePaginatedReportOptions
  [SortConfiguration](#cfn-quicksight-analysis-tableconfiguration-sortconfiguration): 
    TableSortConfiguration
  [TableInlineVisualizations](#cfn-quicksight-analysis-tableconfiguration-tableinlinevisualizations): 
    - TableInlineVisualization
  [TableOptions](#cfn-quicksight-analysis-tableconfiguration-tableoptions): 
    TableOptions
  [TotalOptions](#cfn-quicksight-analysis-tableconfiguration-totaloptions): 
    TotalOptions
```

## Properties<a name="aws-properties-quicksight-analysis-tableconfiguration-properties"></a>

`FieldOptions`  <a name="cfn-quicksight-analysis-tableconfiguration-fieldoptions"></a>
The field options for a table visual\.  
*Required*: No  
*Type*: [TableFieldOptions](aws-properties-quicksight-analysis-tablefieldoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-tableconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [TableFieldWells](aws-properties-quicksight-analysis-tablefieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginatedReportOptions`  <a name="cfn-quicksight-analysis-tableconfiguration-paginatedreportoptions"></a>
The paginated report options for a table visual\.  
*Required*: No  
*Type*: [TablePaginatedReportOptions](aws-properties-quicksight-analysis-tablepaginatedreportoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-analysis-tableconfiguration-sortconfiguration"></a>
The sort configuration for a `TableVisual`\.  
*Required*: No  
*Type*: [TableSortConfiguration](aws-properties-quicksight-analysis-tablesortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableInlineVisualizations`  <a name="cfn-quicksight-analysis-tableconfiguration-tableinlinevisualizations"></a>
A collection of inline visualizations to display within a chart\.  
*Required*: No  
*Type*: List of [TableInlineVisualization](aws-properties-quicksight-analysis-tableinlinevisualization.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableOptions`  <a name="cfn-quicksight-analysis-tableconfiguration-tableoptions"></a>
The table options for a table visual\.  
*Required*: No  
*Type*: [TableOptions](aws-properties-quicksight-analysis-tableoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalOptions`  <a name="cfn-quicksight-analysis-tableconfiguration-totaloptions"></a>
The total options for a table visual\.  
*Required*: No  
*Type*: [TotalOptions](aws-properties-quicksight-analysis-totaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)