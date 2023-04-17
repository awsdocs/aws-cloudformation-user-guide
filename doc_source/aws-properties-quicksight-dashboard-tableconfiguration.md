# AWS::QuickSight::Dashboard TableConfiguration<a name="aws-properties-quicksight-dashboard-tableconfiguration"></a>

The configuration for a `TableVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-tableconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tableconfiguration-syntax.json"></a>

```
{
  "[FieldOptions](#cfn-quicksight-dashboard-tableconfiguration-fieldoptions)" : TableFieldOptions,
  "[FieldWells](#cfn-quicksight-dashboard-tableconfiguration-fieldwells)" : TableFieldWells,
  "[PaginatedReportOptions](#cfn-quicksight-dashboard-tableconfiguration-paginatedreportoptions)" : TablePaginatedReportOptions,
  "[SortConfiguration](#cfn-quicksight-dashboard-tableconfiguration-sortconfiguration)" : TableSortConfiguration,
  "[TableInlineVisualizations](#cfn-quicksight-dashboard-tableconfiguration-tableinlinevisualizations)" : [ TableInlineVisualization, ... ],
  "[TableOptions](#cfn-quicksight-dashboard-tableconfiguration-tableoptions)" : TableOptions,
  "[TotalOptions](#cfn-quicksight-dashboard-tableconfiguration-totaloptions)" : TotalOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tableconfiguration-syntax.yaml"></a>

```
  [FieldOptions](#cfn-quicksight-dashboard-tableconfiguration-fieldoptions): 
    TableFieldOptions
  [FieldWells](#cfn-quicksight-dashboard-tableconfiguration-fieldwells): 
    TableFieldWells
  [PaginatedReportOptions](#cfn-quicksight-dashboard-tableconfiguration-paginatedreportoptions): 
    TablePaginatedReportOptions
  [SortConfiguration](#cfn-quicksight-dashboard-tableconfiguration-sortconfiguration): 
    TableSortConfiguration
  [TableInlineVisualizations](#cfn-quicksight-dashboard-tableconfiguration-tableinlinevisualizations): 
    - TableInlineVisualization
  [TableOptions](#cfn-quicksight-dashboard-tableconfiguration-tableoptions): 
    TableOptions
  [TotalOptions](#cfn-quicksight-dashboard-tableconfiguration-totaloptions): 
    TotalOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-tableconfiguration-properties"></a>

`FieldOptions`  <a name="cfn-quicksight-dashboard-tableconfiguration-fieldoptions"></a>
The field options for a table visual\.  
*Required*: No  
*Type*: [TableFieldOptions](aws-properties-quicksight-dashboard-tablefieldoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-tableconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [TableFieldWells](aws-properties-quicksight-dashboard-tablefieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginatedReportOptions`  <a name="cfn-quicksight-dashboard-tableconfiguration-paginatedreportoptions"></a>
The paginated report options for a table visual\.  
*Required*: No  
*Type*: [TablePaginatedReportOptions](aws-properties-quicksight-dashboard-tablepaginatedreportoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-tableconfiguration-sortconfiguration"></a>
The sort configuration for a `TableVisual`\.  
*Required*: No  
*Type*: [TableSortConfiguration](aws-properties-quicksight-dashboard-tablesortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableInlineVisualizations`  <a name="cfn-quicksight-dashboard-tableconfiguration-tableinlinevisualizations"></a>
A collection of inline visualizations to display within a chart\.  
*Required*: No  
*Type*: List of [TableInlineVisualization](aws-properties-quicksight-dashboard-tableinlinevisualization.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableOptions`  <a name="cfn-quicksight-dashboard-tableconfiguration-tableoptions"></a>
The table options for a table visual\.  
*Required*: No  
*Type*: [TableOptions](aws-properties-quicksight-dashboard-tableoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalOptions`  <a name="cfn-quicksight-dashboard-tableconfiguration-totaloptions"></a>
The total options for a table visual\.  
*Required*: No  
*Type*: [TotalOptions](aws-properties-quicksight-dashboard-totaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)