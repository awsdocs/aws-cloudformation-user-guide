# AWS::QuickSight::Dashboard PivotTableSortConfiguration<a name="aws-properties-quicksight-dashboard-pivottablesortconfiguration"></a>

The sort configuration for a `PivotTableVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottablesortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottablesortconfiguration-syntax.json"></a>

```
{
  "[FieldSortOptions](#cfn-quicksight-dashboard-pivottablesortconfiguration-fieldsortoptions)" : [ PivotFieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottablesortconfiguration-syntax.yaml"></a>

```
  [FieldSortOptions](#cfn-quicksight-dashboard-pivottablesortconfiguration-fieldsortoptions): 
    - PivotFieldSortOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottablesortconfiguration-properties"></a>

`FieldSortOptions`  <a name="cfn-quicksight-dashboard-pivottablesortconfiguration-fieldsortoptions"></a>
The field sort options for a pivot table sort configuration\.  
*Required*: No  
*Type*: [List](aws-properties-quicksight-dashboard-fieldsortoptions.md) of [PivotFieldSortOptions](aws-properties-quicksight-dashboard-pivotfieldsortoptions.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)