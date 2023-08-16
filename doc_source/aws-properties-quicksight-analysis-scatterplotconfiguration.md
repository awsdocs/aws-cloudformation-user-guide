# AWS::QuickSight::Analysis ScatterPlotConfiguration<a name="aws-properties-quicksight-analysis-scatterplotconfiguration"></a>

The configuration of a scatter plot\.

## Syntax<a name="aws-properties-quicksight-analysis-scatterplotconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-scatterplotconfiguration-syntax.json"></a>

```
{
  "[DataLabels](#cfn-quicksight-analysis-scatterplotconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-analysis-scatterplotconfiguration-fieldwells)" : ScatterPlotFieldWells,
  "[Legend](#cfn-quicksight-analysis-scatterplotconfiguration-legend)" : LegendOptions,
  "[Tooltip](#cfn-quicksight-analysis-scatterplotconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-analysis-scatterplotconfiguration-visualpalette)" : VisualPalette,
  "[XAxisDisplayOptions](#cfn-quicksight-analysis-scatterplotconfiguration-xaxisdisplayoptions)" : AxisDisplayOptions,
  "[XAxisLabelOptions](#cfn-quicksight-analysis-scatterplotconfiguration-xaxislabeloptions)" : ChartAxisLabelOptions,
  "[YAxisDisplayOptions](#cfn-quicksight-analysis-scatterplotconfiguration-yaxisdisplayoptions)" : AxisDisplayOptions,
  "[YAxisLabelOptions](#cfn-quicksight-analysis-scatterplotconfiguration-yaxislabeloptions)" : ChartAxisLabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-scatterplotconfiguration-syntax.yaml"></a>

```
  [DataLabels](#cfn-quicksight-analysis-scatterplotconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-analysis-scatterplotconfiguration-fieldwells): 
    ScatterPlotFieldWells
  [Legend](#cfn-quicksight-analysis-scatterplotconfiguration-legend): 
    LegendOptions
  [Tooltip](#cfn-quicksight-analysis-scatterplotconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-analysis-scatterplotconfiguration-visualpalette): 
    VisualPalette
  [XAxisDisplayOptions](#cfn-quicksight-analysis-scatterplotconfiguration-xaxisdisplayoptions): 
    AxisDisplayOptions
  [XAxisLabelOptions](#cfn-quicksight-analysis-scatterplotconfiguration-xaxislabeloptions): 
    ChartAxisLabelOptions
  [YAxisDisplayOptions](#cfn-quicksight-analysis-scatterplotconfiguration-yaxisdisplayoptions): 
    AxisDisplayOptions
  [YAxisLabelOptions](#cfn-quicksight-analysis-scatterplotconfiguration-yaxislabeloptions): 
    ChartAxisLabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-scatterplotconfiguration-properties"></a>

`DataLabels`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-analysis-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [ScatterPlotFieldWells](aws-properties-quicksight-analysis-scatterplotfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-analysis-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-tooltip"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-analysis-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-analysis-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisDisplayOptions`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-xaxisdisplayoptions"></a>
The label display options \(grid line, range, scale, and axis step\) of the scatter plot's x\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisLabelOptions`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-xaxislabeloptions"></a>
The label options \(label text, label visibility, and sort icon visibility\) of the scatter plot's x\-axis\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxisDisplayOptions`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-yaxisdisplayoptions"></a>
The label display options \(grid line, range, scale, and axis step\) of the scatter plot's y\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxisLabelOptions`  <a name="cfn-quicksight-analysis-scatterplotconfiguration-yaxislabeloptions"></a>
The label options \(label text, label visibility, and sort icon visibility\) of the scatter plot's y\-axis\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)