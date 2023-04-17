# AWS::QuickSight::Dashboard HeatMapConfiguration<a name="aws-properties-quicksight-dashboard-heatmapconfiguration"></a>

The configuration of a heat map\.

## Syntax<a name="aws-properties-quicksight-dashboard-heatmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-heatmapconfiguration-syntax.json"></a>

```
{
  "[ColorScale](#cfn-quicksight-dashboard-heatmapconfiguration-colorscale)" : ColorScale,
  "[ColumnLabelOptions](#cfn-quicksight-dashboard-heatmapconfiguration-columnlabeloptions)" : ChartAxisLabelOptions,
  "[DataLabels](#cfn-quicksight-dashboard-heatmapconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-dashboard-heatmapconfiguration-fieldwells)" : HeatMapFieldWells,
  "[Legend](#cfn-quicksight-dashboard-heatmapconfiguration-legend)" : LegendOptions,
  "[RowLabelOptions](#cfn-quicksight-dashboard-heatmapconfiguration-rowlabeloptions)" : ChartAxisLabelOptions,
  "[SortConfiguration](#cfn-quicksight-dashboard-heatmapconfiguration-sortconfiguration)" : HeatMapSortConfiguration,
  "[Tooltip](#cfn-quicksight-dashboard-heatmapconfiguration-tooltip)" : TooltipOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-heatmapconfiguration-syntax.yaml"></a>

```
  [ColorScale](#cfn-quicksight-dashboard-heatmapconfiguration-colorscale): 
    ColorScale
  [ColumnLabelOptions](#cfn-quicksight-dashboard-heatmapconfiguration-columnlabeloptions): 
    ChartAxisLabelOptions
  [DataLabels](#cfn-quicksight-dashboard-heatmapconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-dashboard-heatmapconfiguration-fieldwells): 
    HeatMapFieldWells
  [Legend](#cfn-quicksight-dashboard-heatmapconfiguration-legend): 
    LegendOptions
  [RowLabelOptions](#cfn-quicksight-dashboard-heatmapconfiguration-rowlabeloptions): 
    ChartAxisLabelOptions
  [SortConfiguration](#cfn-quicksight-dashboard-heatmapconfiguration-sortconfiguration): 
    HeatMapSortConfiguration
  [Tooltip](#cfn-quicksight-dashboard-heatmapconfiguration-tooltip): 
    TooltipOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-heatmapconfiguration-properties"></a>

`ColorScale`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-colorscale"></a>
The color options \(gradient color, point of divergence\) in a heat map\.  
*Required*: No  
*Type*: [ColorScale](aws-properties-quicksight-dashboard-colorscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnLabelOptions`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-columnlabeloptions"></a>
The label options of the column that is displayed in a heat map\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-dashboard-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [HeatMapFieldWells](aws-properties-quicksight-dashboard-heatmapfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowLabelOptions`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-rowlabeloptions"></a>
The label options of the row that is displayed in a `heat map`\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-sortconfiguration"></a>
The sort configuration of a heat map\.  
*Required*: No  
*Type*: [HeatMapSortConfiguration](aws-properties-quicksight-dashboard-heatmapsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-dashboard-heatmapconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-dashboard-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)