# AWS::QuickSight::Dashboard BarChartConfiguration<a name="aws-properties-quicksight-dashboard-barchartconfiguration"></a>

The configuration of a `BarChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-barchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-barchartconfiguration-syntax.json"></a>

```
{
  "[BarsArrangement](#cfn-quicksight-dashboard-barchartconfiguration-barsarrangement)" : String,
  "[CategoryAxis](#cfn-quicksight-dashboard-barchartconfiguration-categoryaxis)" : AxisDisplayOptions,
  "[CategoryLabelOptions](#cfn-quicksight-dashboard-barchartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[ColorLabelOptions](#cfn-quicksight-dashboard-barchartconfiguration-colorlabeloptions)" : ChartAxisLabelOptions,
  "[ContributionAnalysisDefaults](#cfn-quicksight-dashboard-barchartconfiguration-contributionanalysisdefaults)" : [ ContributionAnalysisDefault, ... ],
  "[DataLabels](#cfn-quicksight-dashboard-barchartconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-dashboard-barchartconfiguration-fieldwells)" : BarChartFieldWells,
  "[Legend](#cfn-quicksight-dashboard-barchartconfiguration-legend)" : LegendOptions,
  "[Orientation](#cfn-quicksight-dashboard-barchartconfiguration-orientation)" : String,
  "[ReferenceLines](#cfn-quicksight-dashboard-barchartconfiguration-referencelines)" : [ ReferenceLine, ... ],
  "[SmallMultiplesOptions](#cfn-quicksight-dashboard-barchartconfiguration-smallmultiplesoptions)" : SmallMultiplesOptions,
  "[SortConfiguration](#cfn-quicksight-dashboard-barchartconfiguration-sortconfiguration)" : BarChartSortConfiguration,
  "[Tooltip](#cfn-quicksight-dashboard-barchartconfiguration-tooltip)" : TooltipOptions,
  "[ValueAxis](#cfn-quicksight-dashboard-barchartconfiguration-valueaxis)" : AxisDisplayOptions,
  "[ValueLabelOptions](#cfn-quicksight-dashboard-barchartconfiguration-valuelabeloptions)" : ChartAxisLabelOptions,
  "[VisualPalette](#cfn-quicksight-dashboard-barchartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-dashboard-barchartconfiguration-syntax.yaml"></a>

```
  [BarsArrangement](#cfn-quicksight-dashboard-barchartconfiguration-barsarrangement): String
  [CategoryAxis](#cfn-quicksight-dashboard-barchartconfiguration-categoryaxis): 
    AxisDisplayOptions
  [CategoryLabelOptions](#cfn-quicksight-dashboard-barchartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [ColorLabelOptions](#cfn-quicksight-dashboard-barchartconfiguration-colorlabeloptions): 
    ChartAxisLabelOptions
  [ContributionAnalysisDefaults](#cfn-quicksight-dashboard-barchartconfiguration-contributionanalysisdefaults): 
    - ContributionAnalysisDefault
  [DataLabels](#cfn-quicksight-dashboard-barchartconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-dashboard-barchartconfiguration-fieldwells): 
    BarChartFieldWells
  [Legend](#cfn-quicksight-dashboard-barchartconfiguration-legend): 
    LegendOptions
  [Orientation](#cfn-quicksight-dashboard-barchartconfiguration-orientation): String
  [ReferenceLines](#cfn-quicksight-dashboard-barchartconfiguration-referencelines): 
    - ReferenceLine
  [SmallMultiplesOptions](#cfn-quicksight-dashboard-barchartconfiguration-smallmultiplesoptions): 
    SmallMultiplesOptions
  [SortConfiguration](#cfn-quicksight-dashboard-barchartconfiguration-sortconfiguration): 
    BarChartSortConfiguration
  [Tooltip](#cfn-quicksight-dashboard-barchartconfiguration-tooltip): 
    TooltipOptions
  [ValueAxis](#cfn-quicksight-dashboard-barchartconfiguration-valueaxis): 
    AxisDisplayOptions
  [ValueLabelOptions](#cfn-quicksight-dashboard-barchartconfiguration-valuelabeloptions): 
    ChartAxisLabelOptions
  [VisualPalette](#cfn-quicksight-dashboard-barchartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-dashboard-barchartconfiguration-properties"></a>

`BarsArrangement`  <a name="cfn-quicksight-dashboard-barchartconfiguration-barsarrangement"></a>
Determines the arrangement of the bars\. The orientation and arrangement of bars determine the type of bar that is used in the visual\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CLUSTERED | STACKED | STACKED_PERCENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxis`  <a name="cfn-quicksight-dashboard-barchartconfiguration-categoryaxis"></a>
The label display options \(grid line, range, scale, axis step\) for bar chart category\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryLabelOptions`  <a name="cfn-quicksight-dashboard-barchartconfiguration-categorylabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) for a bar chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorLabelOptions`  <a name="cfn-quicksight-dashboard-barchartconfiguration-colorlabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) for a color that is used in a bar chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContributionAnalysisDefaults`  <a name="cfn-quicksight-dashboard-barchartconfiguration-contributionanalysisdefaults"></a>
The contribution analysis \(anomaly configuration\) setup of the visual\.  
*Required*: No  
*Type*: List of [ContributionAnalysisDefault](aws-properties-quicksight-dashboard-contributionanalysisdefault.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-dashboard-barchartconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-dashboard-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-barchartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [BarChartFieldWells](aws-properties-quicksight-dashboard-barchartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-barchartconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Orientation`  <a name="cfn-quicksight-dashboard-barchartconfiguration-orientation"></a>
The orientation of the bars in a bar chart visual\. There are two valid values in this structure:  
+  `HORIZONTAL`: Used for charts that have horizontal bars\. Visuals that use this value are horizontal bar charts, horizontal stacked bar charts, and horizontal stacked 100% bar charts\.
+  `VERTICAL`: Used for charts that have vertical bars\. Visuals that use this value are vertical bar charts, vertical stacked bar charts, and vertical stacked 100% bar charts\.
*Required*: No  
*Type*: String  
*Allowed values*: `HORIZONTAL | VERTICAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferenceLines`  <a name="cfn-quicksight-dashboard-barchartconfiguration-referencelines"></a>
The reference line setup of the visual\.  
*Required*: No  
*Type*: List of [ReferenceLine](aws-properties-quicksight-dashboard-referenceline.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesOptions`  <a name="cfn-quicksight-dashboard-barchartconfiguration-smallmultiplesoptions"></a>
The small multiples setup for the visual\.  
*Required*: No  
*Type*: [SmallMultiplesOptions](aws-properties-quicksight-dashboard-smallmultiplesoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-barchartconfiguration-sortconfiguration"></a>
The sort configuration of a `BarChartVisual`\.  
*Required*: No  
*Type*: [BarChartSortConfiguration](aws-properties-quicksight-dashboard-barchartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-dashboard-barchartconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-dashboard-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueAxis`  <a name="cfn-quicksight-dashboard-barchartconfiguration-valueaxis"></a>
The label display options \(grid line, range, scale, axis step\) for a bar chart value\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueLabelOptions`  <a name="cfn-quicksight-dashboard-barchartconfiguration-valuelabeloptions"></a>
The label options \(label text, label visibility and sort icon visibility\) for a bar chart value\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-dashboard-barchartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-dashboard-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)