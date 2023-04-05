# AWS::QuickSight::Template BoxPlotChartConfiguration<a name="aws-properties-quicksight-template-boxplotchartconfiguration"></a>

The configuration of a `BoxPlotVisual`\.

## Syntax<a name="aws-properties-quicksight-template-boxplotchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-boxplotchartconfiguration-syntax.json"></a>

```
{
  "[BoxPlotOptions](#cfn-quicksight-template-boxplotchartconfiguration-boxplotoptions)" : BoxPlotOptions,
  "[CategoryAxis](#cfn-quicksight-template-boxplotchartconfiguration-categoryaxis)" : AxisDisplayOptions,
  "[CategoryLabelOptions](#cfn-quicksight-template-boxplotchartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[FieldWells](#cfn-quicksight-template-boxplotchartconfiguration-fieldwells)" : BoxPlotFieldWells,
  "[Legend](#cfn-quicksight-template-boxplotchartconfiguration-legend)" : LegendOptions,
  "[PrimaryYAxisDisplayOptions](#cfn-quicksight-template-boxplotchartconfiguration-primaryyaxisdisplayoptions)" : AxisDisplayOptions,
  "[PrimaryYAxisLabelOptions](#cfn-quicksight-template-boxplotchartconfiguration-primaryyaxislabeloptions)" : ChartAxisLabelOptions,
  "[ReferenceLines](#cfn-quicksight-template-boxplotchartconfiguration-referencelines)" : [ ReferenceLine, ... ],
  "[SortConfiguration](#cfn-quicksight-template-boxplotchartconfiguration-sortconfiguration)" : BoxPlotSortConfiguration,
  "[Tooltip](#cfn-quicksight-template-boxplotchartconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-template-boxplotchartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-template-boxplotchartconfiguration-syntax.yaml"></a>

```
  [BoxPlotOptions](#cfn-quicksight-template-boxplotchartconfiguration-boxplotoptions): 
    BoxPlotOptions
  [CategoryAxis](#cfn-quicksight-template-boxplotchartconfiguration-categoryaxis): 
    AxisDisplayOptions
  [CategoryLabelOptions](#cfn-quicksight-template-boxplotchartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [FieldWells](#cfn-quicksight-template-boxplotchartconfiguration-fieldwells): 
    BoxPlotFieldWells
  [Legend](#cfn-quicksight-template-boxplotchartconfiguration-legend): 
    LegendOptions
  [PrimaryYAxisDisplayOptions](#cfn-quicksight-template-boxplotchartconfiguration-primaryyaxisdisplayoptions): 
    AxisDisplayOptions
  [PrimaryYAxisLabelOptions](#cfn-quicksight-template-boxplotchartconfiguration-primaryyaxislabeloptions): 
    ChartAxisLabelOptions
  [ReferenceLines](#cfn-quicksight-template-boxplotchartconfiguration-referencelines): 
    - ReferenceLine
  [SortConfiguration](#cfn-quicksight-template-boxplotchartconfiguration-sortconfiguration): 
    BoxPlotSortConfiguration
  [Tooltip](#cfn-quicksight-template-boxplotchartconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-template-boxplotchartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-template-boxplotchartconfiguration-properties"></a>

`BoxPlotOptions`  <a name="cfn-quicksight-template-boxplotchartconfiguration-boxplotoptions"></a>
The box plot chart options for a box plot visual  
*Required*: No  
*Type*: [BoxPlotOptions](aws-properties-quicksight-template-boxplotoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxis`  <a name="cfn-quicksight-template-boxplotchartconfiguration-categoryaxis"></a>
The label display options \(grid line, range, scale, axis step\) of a box plot category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-template-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryLabelOptions`  <a name="cfn-quicksight-template-boxplotchartconfiguration-categorylabeloptions"></a>
The label options \(label text, label visibility and sort Icon visibility\) of a box plot category\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-boxplotchartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [BoxPlotFieldWells](aws-properties-quicksight-template-boxplotfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-template-boxplotchartconfiguration-legend"></a>
Property description not available\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-template-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisDisplayOptions`  <a name="cfn-quicksight-template-boxplotchartconfiguration-primaryyaxisdisplayoptions"></a>
The label display options \(grid line, range, scale, axis step\) of a box plot category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-template-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisLabelOptions`  <a name="cfn-quicksight-template-boxplotchartconfiguration-primaryyaxislabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) of a box plot value\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferenceLines`  <a name="cfn-quicksight-template-boxplotchartconfiguration-referencelines"></a>
The reference line setup of the visual\.  
*Required*: No  
*Type*: List of [ReferenceLine](aws-properties-quicksight-template-referenceline.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-template-boxplotchartconfiguration-sortconfiguration"></a>
The sort configuration of a `BoxPlotVisual`\.  
*Required*: No  
*Type*: [BoxPlotSortConfiguration](aws-properties-quicksight-template-boxplotsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-template-boxplotchartconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-template-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-template-boxplotchartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-template-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)