# AWS::QuickSight::Template PivotTableConfiguration<a name="aws-properties-quicksight-template-pivottableconfiguration"></a>

The configuration for a `PivotTableVisual`\.

## Syntax<a name="aws-properties-quicksight-template-pivottableconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivottableconfiguration-syntax.json"></a>

```
{
  "[FieldOptions](#cfn-quicksight-template-pivottableconfiguration-fieldoptions)" : PivotTableFieldOptions,
  "[FieldWells](#cfn-quicksight-template-pivottableconfiguration-fieldwells)" : PivotTableFieldWells,
  "[PaginatedReportOptions](#cfn-quicksight-template-pivottableconfiguration-paginatedreportoptions)" : PivotTablePaginatedReportOptions,
  "[SortConfiguration](#cfn-quicksight-template-pivottableconfiguration-sortconfiguration)" : PivotTableSortConfiguration,
  "[TableOptions](#cfn-quicksight-template-pivottableconfiguration-tableoptions)" : PivotTableOptions,
  "[TotalOptions](#cfn-quicksight-template-pivottableconfiguration-totaloptions)" : PivotTableTotalOptions
}
```

### YAML<a name="aws-properties-quicksight-template-pivottableconfiguration-syntax.yaml"></a>

```
  [FieldOptions](#cfn-quicksight-template-pivottableconfiguration-fieldoptions): 
    PivotTableFieldOptions
  [FieldWells](#cfn-quicksight-template-pivottableconfiguration-fieldwells): 
    PivotTableFieldWells
  [PaginatedReportOptions](#cfn-quicksight-template-pivottableconfiguration-paginatedreportoptions): 
    PivotTablePaginatedReportOptions
  [SortConfiguration](#cfn-quicksight-template-pivottableconfiguration-sortconfiguration): 
    PivotTableSortConfiguration
  [TableOptions](#cfn-quicksight-template-pivottableconfiguration-tableoptions): 
    PivotTableOptions
  [TotalOptions](#cfn-quicksight-template-pivottableconfiguration-totaloptions): 
    PivotTableTotalOptions
```

## Properties<a name="aws-properties-quicksight-template-pivottableconfiguration-properties"></a>

`FieldOptions`  <a name="cfn-quicksight-template-pivottableconfiguration-fieldoptions"></a>
The field options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTableFieldOptions](aws-properties-quicksight-template-pivottablefieldoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-pivottableconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [PivotTableFieldWells](aws-properties-quicksight-template-pivottablefieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginatedReportOptions`  <a name="cfn-quicksight-template-pivottableconfiguration-paginatedreportoptions"></a>
The paginated report options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTablePaginatedReportOptions](aws-properties-quicksight-template-pivottablepaginatedreportoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-template-pivottableconfiguration-sortconfiguration"></a>
The sort configuration for a `PivotTableVisual`\.  
*Required*: No  
*Type*: [PivotTableSortConfiguration](aws-properties-quicksight-template-pivottablesortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableOptions`  <a name="cfn-quicksight-template-pivottableconfiguration-tableoptions"></a>
The table options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTableOptions](aws-properties-quicksight-template-pivottableoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalOptions`  <a name="cfn-quicksight-template-pivottableconfiguration-totaloptions"></a>
The total options for a pivot table visual\.  
*Required*: No  
*Type*: [PivotTableTotalOptions](aws-properties-quicksight-template-pivottabletotaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)