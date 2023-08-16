# AWS::QuickSight::Analysis WaterfallChartConfiguration<a name="aws-properties-quicksight-analysis-waterfallchartconfiguration"></a>

The configuration for a waterfall visual\.

## Syntax<a name="aws-properties-quicksight-analysis-waterfallchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-waterfallchartconfiguration-syntax.json"></a>

```
{
  "[CategoryAxisDisplayOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-categoryaxisdisplayoptions)" : AxisDisplayOptions,
  "[CategoryAxisLabelOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-categoryaxislabeloptions)" : ChartAxisLabelOptions,
  "[DataLabels](#cfn-quicksight-analysis-waterfallchartconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-analysis-waterfallchartconfiguration-fieldwells)" : WaterfallChartFieldWells,
  "[Legend](#cfn-quicksight-analysis-waterfallchartconfiguration-legend)" : LegendOptions,
  "[PrimaryYAxisDisplayOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-primaryyaxisdisplayoptions)" : AxisDisplayOptions,
  "[PrimaryYAxisLabelOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-primaryyaxislabeloptions)" : ChartAxisLabelOptions,
  "[SortConfiguration](#cfn-quicksight-analysis-waterfallchartconfiguration-sortconfiguration)" : WaterfallChartSortConfiguration,
  "[VisualPalette](#cfn-quicksight-analysis-waterfallchartconfiguration-visualpalette)" : VisualPalette,
  "[WaterfallChartOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-waterfallchartoptions)" : WaterfallChartOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-waterfallchartconfiguration-syntax.yaml"></a>

```
  [CategoryAxisDisplayOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-categoryaxisdisplayoptions): 
    AxisDisplayOptions
  [CategoryAxisLabelOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-categoryaxislabeloptions): 
    ChartAxisLabelOptions
  [DataLabels](#cfn-quicksight-analysis-waterfallchartconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-analysis-waterfallchartconfiguration-fieldwells): 
    WaterfallChartFieldWells
  [Legend](#cfn-quicksight-analysis-waterfallchartconfiguration-legend): 
    LegendOptions
  [PrimaryYAxisDisplayOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-primaryyaxisdisplayoptions): 
    AxisDisplayOptions
  [PrimaryYAxisLabelOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-primaryyaxislabeloptions): 
    ChartAxisLabelOptions
  [SortConfiguration](#cfn-quicksight-analysis-waterfallchartconfiguration-sortconfiguration): 
    WaterfallChartSortConfiguration
  [VisualPalette](#cfn-quicksight-analysis-waterfallchartconfiguration-visualpalette): 
    VisualPalette
  [WaterfallChartOptions](#cfn-quicksight-analysis-waterfallchartconfiguration-waterfallchartoptions): 
    WaterfallChartOptions
```

## Properties<a name="aws-properties-quicksight-analysis-waterfallchartconfiguration-properties"></a>

`CategoryAxisDisplayOptions`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-categoryaxisdisplayoptions"></a>
The options that determine the presentation of the category axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxisLabelOptions`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-categoryaxislabeloptions"></a>
The options that determine the presentation of the category axis label\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-datalabels"></a>
The data label configuration of a waterfall visual\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-analysis-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-fieldwells"></a>
The field well configuration of a waterfall visual\.  
*Required*: No  
*Type*: [WaterfallChartFieldWells](aws-properties-quicksight-analysis-waterfallchartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-legend"></a>
The legend configuration of a waterfall visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-analysis-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisDisplayOptions`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-primaryyaxisdisplayoptions"></a>
The options that determine the presentation of the y\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-analysis-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisLabelOptions`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-primaryyaxislabeloptions"></a>
The options that determine the presentation of the y\-axis label\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-analysis-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-sortconfiguration"></a>
The sort configuration of a waterfall visual\.  
*Required*: No  
*Type*: [WaterfallChartSortConfiguration](aws-properties-quicksight-analysis-waterfallchartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-visualpalette"></a>
The visual palette configuration of a waterfall visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-analysis-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaterfallChartOptions`  <a name="cfn-quicksight-analysis-waterfallchartconfiguration-waterfallchartoptions"></a>
The options that determine the presentation of a waterfall visual\.  
*Required*: No  
*Type*: [WaterfallChartOptions](aws-properties-quicksight-analysis-waterfallchartoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)