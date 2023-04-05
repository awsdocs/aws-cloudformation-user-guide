# AWS::QuickSight::Dashboard TreeMapConfiguration<a name="aws-properties-quicksight-dashboard-treemapconfiguration"></a>

The configuration of a tree map\.

## Syntax<a name="aws-properties-quicksight-dashboard-treemapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-treemapconfiguration-syntax.json"></a>

```
{
  "[ColorLabelOptions](#cfn-quicksight-dashboard-treemapconfiguration-colorlabeloptions)" : ChartAxisLabelOptions,
  "[ColorScale](#cfn-quicksight-dashboard-treemapconfiguration-colorscale)" : ColorScale,
  "[DataLabels](#cfn-quicksight-dashboard-treemapconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-dashboard-treemapconfiguration-fieldwells)" : TreeMapFieldWells,
  "[GroupLabelOptions](#cfn-quicksight-dashboard-treemapconfiguration-grouplabeloptions)" : ChartAxisLabelOptions,
  "[Legend](#cfn-quicksight-dashboard-treemapconfiguration-legend)" : LegendOptions,
  "[SizeLabelOptions](#cfn-quicksight-dashboard-treemapconfiguration-sizelabeloptions)" : ChartAxisLabelOptions,
  "[SortConfiguration](#cfn-quicksight-dashboard-treemapconfiguration-sortconfiguration)" : TreeMapSortConfiguration,
  "[Tooltip](#cfn-quicksight-dashboard-treemapconfiguration-tooltip)" : TooltipOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-treemapconfiguration-syntax.yaml"></a>

```
  [ColorLabelOptions](#cfn-quicksight-dashboard-treemapconfiguration-colorlabeloptions): 
    ChartAxisLabelOptions
  [ColorScale](#cfn-quicksight-dashboard-treemapconfiguration-colorscale): 
    ColorScale
  [DataLabels](#cfn-quicksight-dashboard-treemapconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-dashboard-treemapconfiguration-fieldwells): 
    TreeMapFieldWells
  [GroupLabelOptions](#cfn-quicksight-dashboard-treemapconfiguration-grouplabeloptions): 
    ChartAxisLabelOptions
  [Legend](#cfn-quicksight-dashboard-treemapconfiguration-legend): 
    LegendOptions
  [SizeLabelOptions](#cfn-quicksight-dashboard-treemapconfiguration-sizelabeloptions): 
    ChartAxisLabelOptions
  [SortConfiguration](#cfn-quicksight-dashboard-treemapconfiguration-sortconfiguration): 
    TreeMapSortConfiguration
  [Tooltip](#cfn-quicksight-dashboard-treemapconfiguration-tooltip): 
    TooltipOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-treemapconfiguration-properties"></a>

`ColorLabelOptions`  <a name="cfn-quicksight-dashboard-treemapconfiguration-colorlabeloptions"></a>
The label options \(label text, label visibility\) for the colors displayed in a tree map\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorScale`  <a name="cfn-quicksight-dashboard-treemapconfiguration-colorscale"></a>
The color options \(gradient color, point of divergence\) of a tree map\.  
*Required*: No  
*Type*: [ColorScale](aws-properties-quicksight-dashboard-colorscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-dashboard-treemapconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-dashboard-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-treemapconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [TreeMapFieldWells](aws-properties-quicksight-dashboard-treemapfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupLabelOptions`  <a name="cfn-quicksight-dashboard-treemapconfiguration-grouplabeloptions"></a>
The label options \(label text, label visibility\) of the groups that are displayed in a tree map\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-treemapconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeLabelOptions`  <a name="cfn-quicksight-dashboard-treemapconfiguration-sizelabeloptions"></a>
The label options \(label text, label visibility\) of the sizes that are displayed in a tree map\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-treemapconfiguration-sortconfiguration"></a>
The sort configuration of a tree map\.  
*Required*: No  
*Type*: [TreeMapSortConfiguration](aws-properties-quicksight-dashboard-treemapsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-dashboard-treemapconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-dashboard-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)