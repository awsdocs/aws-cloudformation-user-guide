# AWS::QuickSight::Template HistogramConfiguration<a name="aws-properties-quicksight-template-histogramconfiguration"></a>

The configuration for a `HistogramVisual`\.

## Syntax<a name="aws-properties-quicksight-template-histogramconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-histogramconfiguration-syntax.json"></a>

```
{
  "[BinOptions](#cfn-quicksight-template-histogramconfiguration-binoptions)" : HistogramBinOptions,
  "[DataLabels](#cfn-quicksight-template-histogramconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-template-histogramconfiguration-fieldwells)" : HistogramFieldWells,
  "[Tooltip](#cfn-quicksight-template-histogramconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-template-histogramconfiguration-visualpalette)" : VisualPalette,
  "[XAxisDisplayOptions](#cfn-quicksight-template-histogramconfiguration-xaxisdisplayoptions)" : AxisDisplayOptions,
  "[XAxisLabelOptions](#cfn-quicksight-template-histogramconfiguration-xaxislabeloptions)" : ChartAxisLabelOptions,
  "[YAxisDisplayOptions](#cfn-quicksight-template-histogramconfiguration-yaxisdisplayoptions)" : AxisDisplayOptions
}
```

### YAML<a name="aws-properties-quicksight-template-histogramconfiguration-syntax.yaml"></a>

```
  [BinOptions](#cfn-quicksight-template-histogramconfiguration-binoptions): 
    HistogramBinOptions
  [DataLabels](#cfn-quicksight-template-histogramconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-template-histogramconfiguration-fieldwells): 
    HistogramFieldWells
  [Tooltip](#cfn-quicksight-template-histogramconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-template-histogramconfiguration-visualpalette): 
    VisualPalette
  [XAxisDisplayOptions](#cfn-quicksight-template-histogramconfiguration-xaxisdisplayoptions): 
    AxisDisplayOptions
  [XAxisLabelOptions](#cfn-quicksight-template-histogramconfiguration-xaxislabeloptions): 
    ChartAxisLabelOptions
  [YAxisDisplayOptions](#cfn-quicksight-template-histogramconfiguration-yaxisdisplayoptions): 
    AxisDisplayOptions
```

## Properties<a name="aws-properties-quicksight-template-histogramconfiguration-properties"></a>

`BinOptions`  <a name="cfn-quicksight-template-histogramconfiguration-binoptions"></a>
The options that determine the presentation of histogram bins\.  
*Required*: No  
*Type*: [HistogramBinOptions](aws-properties-quicksight-template-histogrambinoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-template-histogramconfiguration-datalabels"></a>
The data label configuration of a histogram\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-template-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-histogramconfiguration-fieldwells"></a>
The field well configuration of a histogram\.  
*Required*: No  
*Type*: [HistogramFieldWells](aws-properties-quicksight-template-histogramfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-template-histogramconfiguration-tooltip"></a>
The tooltip configuration of a histogram\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-template-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-template-histogramconfiguration-visualpalette"></a>
The visual palette configuration of a histogram\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-template-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisDisplayOptions`  <a name="cfn-quicksight-template-histogramconfiguration-xaxisdisplayoptions"></a>
The options that determine the presentation of the x\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-template-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisLabelOptions`  <a name="cfn-quicksight-template-histogramconfiguration-xaxislabeloptions"></a>
The options that determine the presentation of the x\-axis label\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxisDisplayOptions`  <a name="cfn-quicksight-template-histogramconfiguration-yaxisdisplayoptions"></a>
The options that determine the presentation of the y\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-template-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)