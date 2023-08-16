# AWS::QuickSight::Dashboard HeatMapSortConfiguration<a name="aws-properties-quicksight-dashboard-heatmapsortconfiguration"></a>

The sort configuration of a heat map\.

## Syntax<a name="aws-properties-quicksight-dashboard-heatmapsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-heatmapsortconfiguration-syntax.json"></a>

```
{
  "[HeatMapColumnItemsLimitConfiguration](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmapcolumnitemslimitconfiguration)" : ItemsLimitConfiguration,
  "[HeatMapColumnSort](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmapcolumnsort)" : [ FieldSortOptions, ... ],
  "[HeatMapRowItemsLimitConfiguration](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmaprowitemslimitconfiguration)" : ItemsLimitConfiguration,
  "[HeatMapRowSort](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmaprowsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-heatmapsortconfiguration-syntax.yaml"></a>

```
  [HeatMapColumnItemsLimitConfiguration](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmapcolumnitemslimitconfiguration): 
    ItemsLimitConfiguration
  [HeatMapColumnSort](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmapcolumnsort): 
    - FieldSortOptions
  [HeatMapRowItemsLimitConfiguration](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmaprowitemslimitconfiguration): 
    ItemsLimitConfiguration
  [HeatMapRowSort](#cfn-quicksight-dashboard-heatmapsortconfiguration-heatmaprowsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-heatmapsortconfiguration-properties"></a>

`HeatMapColumnItemsLimitConfiguration`  <a name="cfn-quicksight-dashboard-heatmapsortconfiguration-heatmapcolumnitemslimitconfiguration"></a>
The limit on the number of columns that are displayed in a heat map\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-dashboard-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapColumnSort`  <a name="cfn-quicksight-dashboard-heatmapsortconfiguration-heatmapcolumnsort"></a>
The column sort configuration for heat map for columns that aren't a part of a field well\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapRowItemsLimitConfiguration`  <a name="cfn-quicksight-dashboard-heatmapsortconfiguration-heatmaprowitemslimitconfiguration"></a>
The limit on the number of rows that are displayed in a heat map\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-dashboard-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapRowSort`  <a name="cfn-quicksight-dashboard-heatmapsortconfiguration-heatmaprowsort"></a>
The field sort configuration of the rows fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)