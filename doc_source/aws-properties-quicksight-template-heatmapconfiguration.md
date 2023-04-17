# AWS::QuickSight::Template HeatMapConfiguration<a name="aws-properties-quicksight-template-heatmapconfiguration"></a>

The configuration of a heat map\.

## Syntax<a name="aws-properties-quicksight-template-heatmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-heatmapconfiguration-syntax.json"></a>

```
{
  "[ColorScale](#cfn-quicksight-template-heatmapconfiguration-colorscale)" : ColorScale,
  "[ColumnLabelOptions](#cfn-quicksight-template-heatmapconfiguration-columnlabeloptions)" : ChartAxisLabelOptions,
  "[DataLabels](#cfn-quicksight-template-heatmapconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-template-heatmapconfiguration-fieldwells)" : HeatMapFieldWells,
  "[Legend](#cfn-quicksight-template-heatmapconfiguration-legend)" : LegendOptions,
  "[RowLabelOptions](#cfn-quicksight-template-heatmapconfiguration-rowlabeloptions)" : ChartAxisLabelOptions,
  "[SortConfiguration](#cfn-quicksight-template-heatmapconfiguration-sortconfiguration)" : HeatMapSortConfiguration,
  "[Tooltip](#cfn-quicksight-template-heatmapconfiguration-tooltip)" : TooltipOptions
}
```

### YAML<a name="aws-properties-quicksight-template-heatmapconfiguration-syntax.yaml"></a>

```
  [ColorScale](#cfn-quicksight-template-heatmapconfiguration-colorscale): 
    ColorScale
  [ColumnLabelOptions](#cfn-quicksight-template-heatmapconfiguration-columnlabeloptions): 
    ChartAxisLabelOptions
  [DataLabels](#cfn-quicksight-template-heatmapconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-template-heatmapconfiguration-fieldwells): 
    HeatMapFieldWells
  [Legend](#cfn-quicksight-template-heatmapconfiguration-legend): 
    LegendOptions
  [RowLabelOptions](#cfn-quicksight-template-heatmapconfiguration-rowlabeloptions): 
    ChartAxisLabelOptions
  [SortConfiguration](#cfn-quicksight-template-heatmapconfiguration-sortconfiguration): 
    HeatMapSortConfiguration
  [Tooltip](#cfn-quicksight-template-heatmapconfiguration-tooltip): 
    TooltipOptions
```

## Properties<a name="aws-properties-quicksight-template-heatmapconfiguration-properties"></a>

`ColorScale`  <a name="cfn-quicksight-template-heatmapconfiguration-colorscale"></a>
The color options \(gradient color, point of divergence\) in a heat map\.  
*Required*: No  
*Type*: [ColorScale](aws-properties-quicksight-template-colorscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnLabelOptions`  <a name="cfn-quicksight-template-heatmapconfiguration-columnlabeloptions"></a>
The label options of the column that is displayed in a heat map\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-template-heatmapconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-template-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-heatmapconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [HeatMapFieldWells](aws-properties-quicksight-template-heatmapfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-template-heatmapconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-template-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowLabelOptions`  <a name="cfn-quicksight-template-heatmapconfiguration-rowlabeloptions"></a>
The label options of the row that is displayed in a `heat map`\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-template-heatmapconfiguration-sortconfiguration"></a>
The sort configuration of a heat map\.  
*Required*: No  
*Type*: [HeatMapSortConfiguration](aws-properties-quicksight-template-heatmapsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-template-heatmapconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-template-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)