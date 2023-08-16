# AWS::QuickSight::Analysis BoxPlotChartConfiguration<a name="aws-properties-quicksight-analysis-boxplotchartconfiguration"></a>

The configuration of a `BoxPlotVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-boxplotchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-boxplotchartconfiguration-syntax.json"></a>

```
{
  "[BoxPlotOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-boxplotoptions)" : BoxPlotOptions,
  "[CategoryAxis](#cfn-quicksight-analysis-boxplotchartconfiguration-categoryaxis)" : AxisDisplayOptions,
  "[CategoryLabelOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[FieldWells](#cfn-quicksight-analysis-boxplotchartconfiguration-fieldwells)" : BoxPlotFieldWells,
  "[Legend](#cfn-quicksight-analysis-boxplotchartconfiguration-legend)" : LegendOptions,
  "[PrimaryYAxisDisplayOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-primaryyaxisdisplayoptions)" : AxisDisplayOptions,
  "[PrimaryYAxisLabelOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-primaryyaxislabeloptions)" : ChartAxisLabelOptions,
  "[ReferenceLines](#cfn-quicksight-analysis-boxplotchartconfiguration-referencelines)" : [ ReferenceLine, ... ],
  "[SortConfiguration](#cfn-quicksight-analysis-boxplotchartconfiguration-sortconfiguration)" : BoxPlotSortConfiguration,
  "[Tooltip](#cfn-quicksight-analysis-boxplotchartconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-analysis-boxplotchartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-analysis-boxplotchartconfiguration-syntax.yaml"></a>

```
  [BoxPlotOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-boxplotoptions): 
    BoxPlotOptions
  [CategoryAxis](#cfn-quicksight-analysis-boxplotchartconfiguration-categoryaxis): 
    AxisDisplayOptions
  [CategoryLabelOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [FieldWells](#cfn-quicksight-analysis-boxplotchartconfiguration-fieldwells): 
    BoxPlotFieldWells
  [Legend](#cfn-quicksight-analysis-boxplotchartconfiguration-legend): 
    LegendOptions
  [PrimaryYAxisDisplayOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-primaryyaxisdisplayoptions): 
    AxisDisplayOptions
  [PrimaryYAxisLabelOptions](#cfn-quicksight-analysis-boxplotchartconfiguration-primaryyaxislabeloptions): 
    ChartAxisLabelOptions
  [ReferenceLines](#cfn-quicksight-analysis-boxplotchartconfiguration-referencelines): 
    - ReferenceLine
  [SortConfiguration](#cfn-quicksight-analysis-boxplotchartconfiguration-sortconfiguration): 
    BoxPlotSortConfiguration
  [Tooltip](#cfn-quicksight-analysis-boxplotchartconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-analysis-boxplotchartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-analysis-boxplotchartconfiguration-properties"></a>

`BoxPlotOptions`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-boxplotoptions"></a>
The box plot chart options for a box plot visual  
*Required*: No  
*Type*: [BoxPlotOptions](aws-properties-quicksight-analysis-boxplotoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxis`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-categoryaxis"></a>
The label display options \(grid line, range, scale, axis step\) of a box plot category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryLabelOptions`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-categorylabeloptions"></a>
The label options \(label text, label visibility and sort Icon visibility\) of a box plot category\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [BoxPlotFieldWells](aws-properties-quicksight-analysis-boxplotfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-legend"></a>
Property description not available\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-analysis-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisDisplayOptions`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-primaryyaxisdisplayoptions"></a>
The label display options \(grid line, range, scale, axis step\) of a box plot category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisLabelOptions`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-primaryyaxislabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) of a box plot value\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferenceLines`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-referencelines"></a>
The reference line setup of the visual\.  
*Required*: No  
*Type*: List of [ReferenceLine](aws-properties-quicksight-analysis-referenceline.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-sortconfiguration"></a>
The sort configuration of a `BoxPlotVisual`\.  
*Required*: No  
*Type*: [BoxPlotSortConfiguration](aws-properties-quicksight-analysis-boxplotsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-analysis-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-analysis-boxplotchartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-analysis-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)