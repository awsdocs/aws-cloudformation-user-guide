# AWS::QuickSight::Dashboard BoxPlotChartConfiguration<a name="aws-properties-quicksight-dashboard-boxplotchartconfiguration"></a>

The configuration of a `BoxPlotVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-boxplotchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-boxplotchartconfiguration-syntax.json"></a>

```
{
  "[BoxPlotOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-boxplotoptions)" : BoxPlotOptions,
  "[CategoryAxis](#cfn-quicksight-dashboard-boxplotchartconfiguration-categoryaxis)" : AxisDisplayOptions,
  "[CategoryLabelOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[FieldWells](#cfn-quicksight-dashboard-boxplotchartconfiguration-fieldwells)" : BoxPlotFieldWells,
  "[Legend](#cfn-quicksight-dashboard-boxplotchartconfiguration-legend)" : LegendOptions,
  "[PrimaryYAxisDisplayOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-primaryyaxisdisplayoptions)" : AxisDisplayOptions,
  "[PrimaryYAxisLabelOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-primaryyaxislabeloptions)" : ChartAxisLabelOptions,
  "[ReferenceLines](#cfn-quicksight-dashboard-boxplotchartconfiguration-referencelines)" : [ ReferenceLine, ... ],
  "[SortConfiguration](#cfn-quicksight-dashboard-boxplotchartconfiguration-sortconfiguration)" : BoxPlotSortConfiguration,
  "[Tooltip](#cfn-quicksight-dashboard-boxplotchartconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-dashboard-boxplotchartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-dashboard-boxplotchartconfiguration-syntax.yaml"></a>

```
  [BoxPlotOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-boxplotoptions): 
    BoxPlotOptions
  [CategoryAxis](#cfn-quicksight-dashboard-boxplotchartconfiguration-categoryaxis): 
    AxisDisplayOptions
  [CategoryLabelOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [FieldWells](#cfn-quicksight-dashboard-boxplotchartconfiguration-fieldwells): 
    BoxPlotFieldWells
  [Legend](#cfn-quicksight-dashboard-boxplotchartconfiguration-legend): 
    LegendOptions
  [PrimaryYAxisDisplayOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-primaryyaxisdisplayoptions): 
    AxisDisplayOptions
  [PrimaryYAxisLabelOptions](#cfn-quicksight-dashboard-boxplotchartconfiguration-primaryyaxislabeloptions): 
    ChartAxisLabelOptions
  [ReferenceLines](#cfn-quicksight-dashboard-boxplotchartconfiguration-referencelines): 
    - ReferenceLine
  [SortConfiguration](#cfn-quicksight-dashboard-boxplotchartconfiguration-sortconfiguration): 
    BoxPlotSortConfiguration
  [Tooltip](#cfn-quicksight-dashboard-boxplotchartconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-dashboard-boxplotchartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-dashboard-boxplotchartconfiguration-properties"></a>

`BoxPlotOptions`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-boxplotoptions"></a>
The box plot chart options for a box plot visual  
*Required*: No  
*Type*: [BoxPlotOptions](aws-properties-quicksight-dashboard-boxplotoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxis`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-categoryaxis"></a>
The label display options \(grid line, range, scale, axis step\) of a box plot category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryLabelOptions`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-categorylabeloptions"></a>
The label options \(label text, label visibility and sort Icon visibility\) of a box plot category\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [BoxPlotFieldWells](aws-properties-quicksight-dashboard-boxplotfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-legend"></a>
Property description not available\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisDisplayOptions`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-primaryyaxisdisplayoptions"></a>
The label display options \(grid line, range, scale, axis step\) of a box plot category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisLabelOptions`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-primaryyaxislabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) of a box plot value\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferenceLines`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-referencelines"></a>
The reference line setup of the visual\.  
*Required*: No  
*Type*: List of [ReferenceLine](aws-properties-quicksight-dashboard-referenceline.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-sortconfiguration"></a>
The sort configuration of a `BoxPlotVisual`\.  
*Required*: No  
*Type*: [BoxPlotSortConfiguration](aws-properties-quicksight-dashboard-boxplotsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-dashboard-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-dashboard-boxplotchartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-dashboard-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)