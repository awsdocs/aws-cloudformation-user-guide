# AWS::QuickSight::Analysis HeatMapSortConfiguration<a name="aws-properties-quicksight-analysis-heatmapsortconfiguration"></a>

The sort configuration of a heat map\.

## Syntax<a name="aws-properties-quicksight-analysis-heatmapsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-heatmapsortconfiguration-syntax.json"></a>

```
{
  "[HeatMapColumnItemsLimitConfiguration](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmapcolumnitemslimitconfiguration)" : ItemsLimitConfiguration,
  "[HeatMapColumnSort](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmapcolumnsort)" : [ FieldSortOptions, ... ],
  "[HeatMapRowItemsLimitConfiguration](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmaprowitemslimitconfiguration)" : ItemsLimitConfiguration,
  "[HeatMapRowSort](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmaprowsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-heatmapsortconfiguration-syntax.yaml"></a>

```
  [HeatMapColumnItemsLimitConfiguration](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmapcolumnitemslimitconfiguration): 
    ItemsLimitConfiguration
  [HeatMapColumnSort](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmapcolumnsort): 
    - FieldSortOptions
  [HeatMapRowItemsLimitConfiguration](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmaprowitemslimitconfiguration): 
    ItemsLimitConfiguration
  [HeatMapRowSort](#cfn-quicksight-analysis-heatmapsortconfiguration-heatmaprowsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-analysis-heatmapsortconfiguration-properties"></a>

`HeatMapColumnItemsLimitConfiguration`  <a name="cfn-quicksight-analysis-heatmapsortconfiguration-heatmapcolumnitemslimitconfiguration"></a>
The limit on the number of columns that are displayed in a heat map\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-analysis-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapColumnSort`  <a name="cfn-quicksight-analysis-heatmapsortconfiguration-heatmapcolumnsort"></a>
The column sort configuration for heat map for columns that aren't a part of a field well\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-analysis-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapRowItemsLimitConfiguration`  <a name="cfn-quicksight-analysis-heatmapsortconfiguration-heatmaprowitemslimitconfiguration"></a>
The limit on the number of rows that are displayed in a heat map\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-analysis-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapRowSort`  <a name="cfn-quicksight-analysis-heatmapsortconfiguration-heatmaprowsort"></a>
The field sort configuration of the rows fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-analysis-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)