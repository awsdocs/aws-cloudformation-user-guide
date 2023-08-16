# AWS::QuickSight::Dashboard ComboChartConfiguration<a name="aws-properties-quicksight-dashboard-combochartconfiguration"></a>

The configuration of a `ComboChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-combochartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-combochartconfiguration-syntax.json"></a>

```
{
  "[BarDataLabels](#cfn-quicksight-dashboard-combochartconfiguration-bardatalabels)" : DataLabelOptions,
  "[BarsArrangement](#cfn-quicksight-dashboard-combochartconfiguration-barsarrangement)" : String,
  "[CategoryAxis](#cfn-quicksight-dashboard-combochartconfiguration-categoryaxis)" : AxisDisplayOptions,
  "[CategoryLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[ColorLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-colorlabeloptions)" : ChartAxisLabelOptions,
  "[FieldWells](#cfn-quicksight-dashboard-combochartconfiguration-fieldwells)" : ComboChartFieldWells,
  "[Legend](#cfn-quicksight-dashboard-combochartconfiguration-legend)" : LegendOptions,
  "[LineDataLabels](#cfn-quicksight-dashboard-combochartconfiguration-linedatalabels)" : DataLabelOptions,
  "[PrimaryYAxisDisplayOptions](#cfn-quicksight-dashboard-combochartconfiguration-primaryyaxisdisplayoptions)" : AxisDisplayOptions,
  "[PrimaryYAxisLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-primaryyaxislabeloptions)" : ChartAxisLabelOptions,
  "[ReferenceLines](#cfn-quicksight-dashboard-combochartconfiguration-referencelines)" : [ ReferenceLine, ... ],
  "[SecondaryYAxisDisplayOptions](#cfn-quicksight-dashboard-combochartconfiguration-secondaryyaxisdisplayoptions)" : AxisDisplayOptions,
  "[SecondaryYAxisLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-secondaryyaxislabeloptions)" : ChartAxisLabelOptions,
  "[SortConfiguration](#cfn-quicksight-dashboard-combochartconfiguration-sortconfiguration)" : ComboChartSortConfiguration,
  "[Tooltip](#cfn-quicksight-dashboard-combochartconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-dashboard-combochartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-dashboard-combochartconfiguration-syntax.yaml"></a>

```
  [BarDataLabels](#cfn-quicksight-dashboard-combochartconfiguration-bardatalabels): 
    DataLabelOptions
  [BarsArrangement](#cfn-quicksight-dashboard-combochartconfiguration-barsarrangement): String
  [CategoryAxis](#cfn-quicksight-dashboard-combochartconfiguration-categoryaxis): 
    AxisDisplayOptions
  [CategoryLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [ColorLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-colorlabeloptions): 
    ChartAxisLabelOptions
  [FieldWells](#cfn-quicksight-dashboard-combochartconfiguration-fieldwells): 
    ComboChartFieldWells
  [Legend](#cfn-quicksight-dashboard-combochartconfiguration-legend): 
    LegendOptions
  [LineDataLabels](#cfn-quicksight-dashboard-combochartconfiguration-linedatalabels): 
    DataLabelOptions
  [PrimaryYAxisDisplayOptions](#cfn-quicksight-dashboard-combochartconfiguration-primaryyaxisdisplayoptions): 
    AxisDisplayOptions
  [PrimaryYAxisLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-primaryyaxislabeloptions): 
    ChartAxisLabelOptions
  [ReferenceLines](#cfn-quicksight-dashboard-combochartconfiguration-referencelines): 
    - ReferenceLine
  [SecondaryYAxisDisplayOptions](#cfn-quicksight-dashboard-combochartconfiguration-secondaryyaxisdisplayoptions): 
    AxisDisplayOptions
  [SecondaryYAxisLabelOptions](#cfn-quicksight-dashboard-combochartconfiguration-secondaryyaxislabeloptions): 
    ChartAxisLabelOptions
  [SortConfiguration](#cfn-quicksight-dashboard-combochartconfiguration-sortconfiguration): 
    ComboChartSortConfiguration
  [Tooltip](#cfn-quicksight-dashboard-combochartconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-dashboard-combochartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-dashboard-combochartconfiguration-properties"></a>

`BarDataLabels`  <a name="cfn-quicksight-dashboard-combochartconfiguration-bardatalabels"></a>
The options that determine if visual data labels are displayed\.  
The data label options for a bar in a combo chart\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-dashboard-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BarsArrangement`  <a name="cfn-quicksight-dashboard-combochartconfiguration-barsarrangement"></a>
Determines the bar arrangement in a combo chart\. The following are valid values in this structure:  
+  `CLUSTERED`: For clustered bar combo charts\.
+  `STACKED`: For stacked bar combo charts\.
+  `STACKED_PERCENT`: Do not use\. If you use this value, the operation returns a validation error\.
*Required*: No  
*Type*: String  
*Allowed values*: `CLUSTERED | STACKED | STACKED_PERCENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxis`  <a name="cfn-quicksight-dashboard-combochartconfiguration-categoryaxis"></a>
The category axis of a combo chart\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryLabelOptions`  <a name="cfn-quicksight-dashboard-combochartconfiguration-categorylabeloptions"></a>
The label options \(label text, label visibility, and sort icon visibility\) of a combo chart category \(group/color\) field well\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorLabelOptions`  <a name="cfn-quicksight-dashboard-combochartconfiguration-colorlabeloptions"></a>
The label options \(label text, label visibility, and sort icon visibility\) of a combo chart's color field well\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-combochartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [ComboChartFieldWells](aws-properties-quicksight-dashboard-combochartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-combochartconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineDataLabels`  <a name="cfn-quicksight-dashboard-combochartconfiguration-linedatalabels"></a>
The options that determine if visual data labels are displayed\.  
The data label options for a line in a combo chart\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-dashboard-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisDisplayOptions`  <a name="cfn-quicksight-dashboard-combochartconfiguration-primaryyaxisdisplayoptions"></a>
The label display options \(grid line, range, scale, and axis step\) of a combo chart's primary y\-axis \(bar\) field well\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisLabelOptions`  <a name="cfn-quicksight-dashboard-combochartconfiguration-primaryyaxislabeloptions"></a>
The label options \(label text, label visibility, and sort icon visibility\) of a combo chart's primary y\-axis \(bar\) field well\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferenceLines`  <a name="cfn-quicksight-dashboard-combochartconfiguration-referencelines"></a>
The reference line setup of the visual\.  
*Required*: No  
*Type*: List of [ReferenceLine](aws-properties-quicksight-dashboard-referenceline.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryYAxisDisplayOptions`  <a name="cfn-quicksight-dashboard-combochartconfiguration-secondaryyaxisdisplayoptions"></a>
The label display options \(grid line, range, scale, axis step\) of a combo chart's secondary y\-axis \(line\) field well\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryYAxisLabelOptions`  <a name="cfn-quicksight-dashboard-combochartconfiguration-secondaryyaxislabeloptions"></a>
The label options \(label text, label visibility, and sort icon visibility\) of a combo chart's secondary y\-axis\(line\) field well\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-combochartconfiguration-sortconfiguration"></a>
The sort configuration of a `ComboChartVisual`\.  
*Required*: No  
*Type*: [ComboChartSortConfiguration](aws-properties-quicksight-dashboard-combochartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-dashboard-combochartconfiguration-tooltip"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-dashboard-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-dashboard-combochartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-dashboard-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)