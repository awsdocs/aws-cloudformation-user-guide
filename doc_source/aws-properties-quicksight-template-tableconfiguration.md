# AWS::QuickSight::Template TableConfiguration<a name="aws-properties-quicksight-template-tableconfiguration"></a>

The configuration for a `TableVisual`\.

## Syntax<a name="aws-properties-quicksight-template-tableconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tableconfiguration-syntax.json"></a>

```
{
  "[FieldOptions](#cfn-quicksight-template-tableconfiguration-fieldoptions)" : TableFieldOptions,
  "[FieldWells](#cfn-quicksight-template-tableconfiguration-fieldwells)" : TableFieldWells,
  "[PaginatedReportOptions](#cfn-quicksight-template-tableconfiguration-paginatedreportoptions)" : TablePaginatedReportOptions,
  "[SortConfiguration](#cfn-quicksight-template-tableconfiguration-sortconfiguration)" : TableSortConfiguration,
  "[TableInlineVisualizations](#cfn-quicksight-template-tableconfiguration-tableinlinevisualizations)" : [ TableInlineVisualization, ... ],
  "[TableOptions](#cfn-quicksight-template-tableconfiguration-tableoptions)" : TableOptions,
  "[TotalOptions](#cfn-quicksight-template-tableconfiguration-totaloptions)" : TotalOptions
}
```

### YAML<a name="aws-properties-quicksight-template-tableconfiguration-syntax.yaml"></a>

```
  [FieldOptions](#cfn-quicksight-template-tableconfiguration-fieldoptions): 
    TableFieldOptions
  [FieldWells](#cfn-quicksight-template-tableconfiguration-fieldwells): 
    TableFieldWells
  [PaginatedReportOptions](#cfn-quicksight-template-tableconfiguration-paginatedreportoptions): 
    TablePaginatedReportOptions
  [SortConfiguration](#cfn-quicksight-template-tableconfiguration-sortconfiguration): 
    TableSortConfiguration
  [TableInlineVisualizations](#cfn-quicksight-template-tableconfiguration-tableinlinevisualizations): 
    - TableInlineVisualization
  [TableOptions](#cfn-quicksight-template-tableconfiguration-tableoptions): 
    TableOptions
  [TotalOptions](#cfn-quicksight-template-tableconfiguration-totaloptions): 
    TotalOptions
```

## Properties<a name="aws-properties-quicksight-template-tableconfiguration-properties"></a>

`FieldOptions`  <a name="cfn-quicksight-template-tableconfiguration-fieldoptions"></a>
The field options for a table visual\.  
*Required*: No  
*Type*: [TableFieldOptions](aws-properties-quicksight-template-tablefieldoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-tableconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [TableFieldWells](aws-properties-quicksight-template-tablefieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginatedReportOptions`  <a name="cfn-quicksight-template-tableconfiguration-paginatedreportoptions"></a>
The paginated report options for a table visual\.  
*Required*: No  
*Type*: [TablePaginatedReportOptions](aws-properties-quicksight-template-tablepaginatedreportoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-template-tableconfiguration-sortconfiguration"></a>
The sort configuration for a `TableVisual`\.  
*Required*: No  
*Type*: [TableSortConfiguration](aws-properties-quicksight-template-tablesortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableInlineVisualizations`  <a name="cfn-quicksight-template-tableconfiguration-tableinlinevisualizations"></a>
A collection of inline visualizations to display within a chart\.  
*Required*: No  
*Type*: List of [TableInlineVisualization](aws-properties-quicksight-template-tableinlinevisualization.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableOptions`  <a name="cfn-quicksight-template-tableconfiguration-tableoptions"></a>
The table options for a table visual\.  
*Required*: No  
*Type*: [TableOptions](aws-properties-quicksight-template-tableoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalOptions`  <a name="cfn-quicksight-template-tableconfiguration-totaloptions"></a>
The total options for a table visual\.  
*Required*: No  
*Type*: [TotalOptions](aws-properties-quicksight-template-totaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)