# AWS::QuickSight::Analysis HistogramConfiguration<a name="aws-properties-quicksight-analysis-histogramconfiguration"></a>

The configuration for a `HistogramVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-histogramconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-histogramconfiguration-syntax.json"></a>

```
{
  "[BinOptions](#cfn-quicksight-analysis-histogramconfiguration-binoptions)" : HistogramBinOptions,
  "[DataLabels](#cfn-quicksight-analysis-histogramconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-analysis-histogramconfiguration-fieldwells)" : HistogramFieldWells,
  "[Tooltip](#cfn-quicksight-analysis-histogramconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-analysis-histogramconfiguration-visualpalette)" : VisualPalette,
  "[XAxisDisplayOptions](#cfn-quicksight-analysis-histogramconfiguration-xaxisdisplayoptions)" : AxisDisplayOptions,
  "[XAxisLabelOptions](#cfn-quicksight-analysis-histogramconfiguration-xaxislabeloptions)" : ChartAxisLabelOptions,
  "[YAxisDisplayOptions](#cfn-quicksight-analysis-histogramconfiguration-yaxisdisplayoptions)" : AxisDisplayOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-histogramconfiguration-syntax.yaml"></a>

```
  [BinOptions](#cfn-quicksight-analysis-histogramconfiguration-binoptions): 
    HistogramBinOptions
  [DataLabels](#cfn-quicksight-analysis-histogramconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-analysis-histogramconfiguration-fieldwells): 
    HistogramFieldWells
  [Tooltip](#cfn-quicksight-analysis-histogramconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-analysis-histogramconfiguration-visualpalette): 
    VisualPalette
  [XAxisDisplayOptions](#cfn-quicksight-analysis-histogramconfiguration-xaxisdisplayoptions): 
    AxisDisplayOptions
  [XAxisLabelOptions](#cfn-quicksight-analysis-histogramconfiguration-xaxislabeloptions): 
    ChartAxisLabelOptions
  [YAxisDisplayOptions](#cfn-quicksight-analysis-histogramconfiguration-yaxisdisplayoptions): 
    AxisDisplayOptions
```

## Properties<a name="aws-properties-quicksight-analysis-histogramconfiguration-properties"></a>

`BinOptions`  <a name="cfn-quicksight-analysis-histogramconfiguration-binoptions"></a>
The options that determine the presentation of histogram bins\.  
*Required*: No  
*Type*: [HistogramBinOptions](aws-properties-quicksight-analysis-histogrambinoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-analysis-histogramconfiguration-datalabels"></a>
The data label configuration of a histogram\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-analysis-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-histogramconfiguration-fieldwells"></a>
The field well configuration of a histogram\.  
*Required*: No  
*Type*: [HistogramFieldWells](aws-properties-quicksight-analysis-histogramfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-analysis-histogramconfiguration-tooltip"></a>
The tooltip configuration of a histogram\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-analysis-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-analysis-histogramconfiguration-visualpalette"></a>
The visual palette configuration of a histogram\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-analysis-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisDisplayOptions`  <a name="cfn-quicksight-analysis-histogramconfiguration-xaxisdisplayoptions"></a>
The options that determine the presentation of the x\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisLabelOptions`  <a name="cfn-quicksight-analysis-histogramconfiguration-xaxislabeloptions"></a>
The options that determine the presentation of the x\-axis label\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxisDisplayOptions`  <a name="cfn-quicksight-analysis-histogramconfiguration-yaxisdisplayoptions"></a>
The options that determine the presentation of the y\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)