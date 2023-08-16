# AWS::QuickSight::Analysis BarChartConfiguration<a name="aws-properties-quicksight-analysis-barchartconfiguration"></a>

The configuration of a `BarChartVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-barchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-barchartconfiguration-syntax.json"></a>

```
{
  "[BarsArrangement](#cfn-quicksight-analysis-barchartconfiguration-barsarrangement)" : String,
  "[CategoryAxis](#cfn-quicksight-analysis-barchartconfiguration-categoryaxis)" : AxisDisplayOptions,
  "[CategoryLabelOptions](#cfn-quicksight-analysis-barchartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[ColorLabelOptions](#cfn-quicksight-analysis-barchartconfiguration-colorlabeloptions)" : ChartAxisLabelOptions,
  "[ContributionAnalysisDefaults](#cfn-quicksight-analysis-barchartconfiguration-contributionanalysisdefaults)" : [ ContributionAnalysisDefault, ... ],
  "[DataLabels](#cfn-quicksight-analysis-barchartconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-analysis-barchartconfiguration-fieldwells)" : BarChartFieldWells,
  "[Legend](#cfn-quicksight-analysis-barchartconfiguration-legend)" : LegendOptions,
  "[Orientation](#cfn-quicksight-analysis-barchartconfiguration-orientation)" : String,
  "[ReferenceLines](#cfn-quicksight-analysis-barchartconfiguration-referencelines)" : [ ReferenceLine, ... ],
  "[SmallMultiplesOptions](#cfn-quicksight-analysis-barchartconfiguration-smallmultiplesoptions)" : SmallMultiplesOptions,
  "[SortConfiguration](#cfn-quicksight-analysis-barchartconfiguration-sortconfiguration)" : BarChartSortConfiguration,
  "[Tooltip](#cfn-quicksight-analysis-barchartconfiguration-tooltip)" : TooltipOptions,
  "[ValueAxis](#cfn-quicksight-analysis-barchartconfiguration-valueaxis)" : AxisDisplayOptions,
  "[ValueLabelOptions](#cfn-quicksight-analysis-barchartconfiguration-valuelabeloptions)" : ChartAxisLabelOptions,
  "[VisualPalette](#cfn-quicksight-analysis-barchartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-analysis-barchartconfiguration-syntax.yaml"></a>

```
  [BarsArrangement](#cfn-quicksight-analysis-barchartconfiguration-barsarrangement): String
  [CategoryAxis](#cfn-quicksight-analysis-barchartconfiguration-categoryaxis): 
    AxisDisplayOptions
  [CategoryLabelOptions](#cfn-quicksight-analysis-barchartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [ColorLabelOptions](#cfn-quicksight-analysis-barchartconfiguration-colorlabeloptions): 
    ChartAxisLabelOptions
  [ContributionAnalysisDefaults](#cfn-quicksight-analysis-barchartconfiguration-contributionanalysisdefaults): 
    - ContributionAnalysisDefault
  [DataLabels](#cfn-quicksight-analysis-barchartconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-analysis-barchartconfiguration-fieldwells): 
    BarChartFieldWells
  [Legend](#cfn-quicksight-analysis-barchartconfiguration-legend): 
    LegendOptions
  [Orientation](#cfn-quicksight-analysis-barchartconfiguration-orientation): String
  [ReferenceLines](#cfn-quicksight-analysis-barchartconfiguration-referencelines): 
    - ReferenceLine
  [SmallMultiplesOptions](#cfn-quicksight-analysis-barchartconfiguration-smallmultiplesoptions): 
    SmallMultiplesOptions
  [SortConfiguration](#cfn-quicksight-analysis-barchartconfiguration-sortconfiguration): 
    BarChartSortConfiguration
  [Tooltip](#cfn-quicksight-analysis-barchartconfiguration-tooltip): 
    TooltipOptions
  [ValueAxis](#cfn-quicksight-analysis-barchartconfiguration-valueaxis): 
    AxisDisplayOptions
  [ValueLabelOptions](#cfn-quicksight-analysis-barchartconfiguration-valuelabeloptions): 
    ChartAxisLabelOptions
  [VisualPalette](#cfn-quicksight-analysis-barchartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-analysis-barchartconfiguration-properties"></a>

`BarsArrangement`  <a name="cfn-quicksight-analysis-barchartconfiguration-barsarrangement"></a>
Determines the arrangement of the bars\. The orientation and arrangement of bars determine the type of bar that is used in the visual\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CLUSTERED | STACKED | STACKED_PERCENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxis`  <a name="cfn-quicksight-analysis-barchartconfiguration-categoryaxis"></a>
The label display options \(grid line, range, scale, axis step\) for bar chart category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryLabelOptions`  <a name="cfn-quicksight-analysis-barchartconfiguration-categorylabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) for a bar chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorLabelOptions`  <a name="cfn-quicksight-analysis-barchartconfiguration-colorlabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) for a color that is used in a bar chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContributionAnalysisDefaults`  <a name="cfn-quicksight-analysis-barchartconfiguration-contributionanalysisdefaults"></a>
The contribution analysis \(anomaly configuration\) setup of the visual\.  
*Required*: No  
*Type*: List of [ContributionAnalysisDefault](aws-properties-quicksight-analysis-contributionanalysisdefault.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-analysis-barchartconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-analysis-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-barchartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [BarChartFieldWells](aws-properties-quicksight-analysis-barchartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-analysis-barchartconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-analysis-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Orientation`  <a name="cfn-quicksight-analysis-barchartconfiguration-orientation"></a>
The orientation of the bars in a bar chart visual\. There are two valid values in this structure:  
+  `HORIZONTAL`: Used for charts that have horizontal bars\. Visuals that use this value are horizontal bar charts, horizontal stacked bar charts, and horizontal stacked 100% bar charts\.
+  `VERTICAL`: Used for charts that have vertical bars\. Visuals that use this value are vertical bar charts, vertical stacked bar charts, and vertical stacked 100% bar charts\.
*Required*: No  
*Type*: String  
*Allowed values*: `HORIZONTAL | VERTICAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferenceLines`  <a name="cfn-quicksight-analysis-barchartconfiguration-referencelines"></a>
The reference line setup of the visual\.  
*Required*: No  
*Type*: List of [ReferenceLine](aws-properties-quicksight-analysis-referenceline.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesOptions`  <a name="cfn-quicksight-analysis-barchartconfiguration-smallmultiplesoptions"></a>
The small multiples setup for the visual\.  
*Required*: No  
*Type*: [SmallMultiplesOptions](aws-properties-quicksight-analysis-smallmultiplesoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-analysis-barchartconfiguration-sortconfiguration"></a>
The sort configuration of a `BarChartVisual`\.  
*Required*: No  
*Type*: [BarChartSortConfiguration](aws-properties-quicksight-analysis-barchartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-analysis-barchartconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-analysis-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueAxis`  <a name="cfn-quicksight-analysis-barchartconfiguration-valueaxis"></a>
The label display options \(grid line, range, scale, axis step\) for a bar chart value\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueLabelOptions`  <a name="cfn-quicksight-analysis-barchartconfiguration-valuelabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) for a bar chart value\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-analysis-barchartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-analysis-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)