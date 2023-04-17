# AWS::QuickSight::Analysis PivotTableConfiguration<a name="aws-properties-quicksight-analysis-pivottableconfiguration"></a>

The configuration for a `PivotTableVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-pivottableconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-pivottableconfiguration-syntax.json"></a>

```
{
  "[FieldOptions](#cfn-quicksight-analysis-pivottableconfiguration-fieldoptions)" : PivotTableFieldOptions,
  "[FieldWells](#cfn-quicksight-analysis-pivottableconfiguration-fieldwells)" : PivotTableFieldWells,
  "[PaginatedReportOptions](#cfn-quicksight-analysis-pivottableconfiguration-paginatedreportoptions)" : PivotTablePaginatedReportOptions,
  "[SortConfiguration](#cfn-quicksight-analysis-pivottableconfiguration-sortconfiguration)" : PivotTableSortConfiguration,
  "[TableOptions](#cfn-quicksight-analysis-pivottableconfiguration-tableoptions)" : PivotTableOptions,
  "[TotalOptions](#cfn-quicksight-analysis-pivottableconfiguration-totaloptions)" : PivotTableTotalOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-pivottableconfiguration-syntax.yaml"></a>

```
  [FieldOptions](#cfn-quicksight-analysis-pivottableconfiguration-fieldoptions): 
    PivotTableFieldOptions
  [FieldWells](#cfn-quicksight-analysis-pivottableconfiguration-fieldwells): 
    PivotTableFieldWells
  [PaginatedReportOptions](#cfn-quicksight-analysis-pivottableconfiguration-paginatedreportoptions): 
    PivotTablePaginatedReportOptions
  [SortConfiguration](#cfn-quicksight-analysis-pivottableconfiguration-sortconfiguration): 
    PivotTableSortConfiguration
  [TableOptions](#cfn-quicksight-analysis-pivottableconfiguration-tableoptions): 
    PivotTableOptions
  [TotalOptions](#cfn-quicksight-analysis-pivottableconfiguration-totaloptions): 
    PivotTableTotalOptions
```

## Properties<a name="aws-properties-quicksight-analysis-pivottableconfiguration-properties"></a>

`FieldOptions`  <a name="cfn-quicksight-analysis-pivottableconfiguration-fieldoptions"></a>
The field options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTableFieldOptions](aws-properties-quicksight-analysis-pivottablefieldoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-pivottableconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [PivotTableFieldWells](aws-properties-quicksight-analysis-pivottablefieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginatedReportOptions`  <a name="cfn-quicksight-analysis-pivottableconfiguration-paginatedreportoptions"></a>
The paginated report options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTablePaginatedReportOptions](aws-properties-quicksight-analysis-pivottablepaginatedreportoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-analysis-pivottableconfiguration-sortconfiguration"></a>
The sort configuration for a `PivotTableVisual`\.  
*Required*: No  
*Type*: [PivotTableSortConfiguration](aws-properties-quicksight-analysis-pivottablesortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableOptions`  <a name="cfn-quicksight-analysis-pivottableconfiguration-tableoptions"></a>
The table options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTableOptions](aws-properties-quicksight-analysis-pivottableoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalOptions`  <a name="cfn-quicksight-analysis-pivottableconfiguration-totaloptions"></a>
The total options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTableTotalOptions](aws-properties-quicksight-analysis-pivottabletotaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)