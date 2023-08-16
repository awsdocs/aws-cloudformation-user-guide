# AWS::QuickSight::Template WaterfallChartConfiguration<a name="aws-properties-quicksight-template-waterfallchartconfiguration"></a>

The configuration for a waterfall visual\.

## Syntax<a name="aws-properties-quicksight-template-waterfallchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-waterfallchartconfiguration-syntax.json"></a>

```
{
  "[CategoryAxisDisplayOptions](#cfn-quicksight-template-waterfallchartconfiguration-categoryaxisdisplayoptions)" : AxisDisplayOptions,
  "[CategoryAxisLabelOptions](#cfn-quicksight-template-waterfallchartconfiguration-categoryaxislabeloptions)" : ChartAxisLabelOptions,
  "[DataLabels](#cfn-quicksight-template-waterfallchartconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-template-waterfallchartconfiguration-fieldwells)" : WaterfallChartFieldWells,
  "[Legend](#cfn-quicksight-template-waterfallchartconfiguration-legend)" : LegendOptions,
  "[PrimaryYAxisDisplayOptions](#cfn-quicksight-template-waterfallchartconfiguration-primaryyaxisdisplayoptions)" : AxisDisplayOptions,
  "[PrimaryYAxisLabelOptions](#cfn-quicksight-template-waterfallchartconfiguration-primaryyaxislabeloptions)" : ChartAxisLabelOptions,
  "[SortConfiguration](#cfn-quicksight-template-waterfallchartconfiguration-sortconfiguration)" : WaterfallChartSortConfiguration,
  "[VisualPalette](#cfn-quicksight-template-waterfallchartconfiguration-visualpalette)" : VisualPalette,
  "[WaterfallChartOptions](#cfn-quicksight-template-waterfallchartconfiguration-waterfallchartoptions)" : WaterfallChartOptions
}
```

### YAML<a name="aws-properties-quicksight-template-waterfallchartconfiguration-syntax.yaml"></a>

```
  [CategoryAxisDisplayOptions](#cfn-quicksight-template-waterfallchartconfiguration-categoryaxisdisplayoptions): 
    AxisDisplayOptions
  [CategoryAxisLabelOptions](#cfn-quicksight-template-waterfallchartconfiguration-categoryaxislabeloptions): 
    ChartAxisLabelOptions
  [DataLabels](#cfn-quicksight-template-waterfallchartconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-template-waterfallchartconfiguration-fieldwells): 
    WaterfallChartFieldWells
  [Legend](#cfn-quicksight-template-waterfallchartconfiguration-legend): 
    LegendOptions
  [PrimaryYAxisDisplayOptions](#cfn-quicksight-template-waterfallchartconfiguration-primaryyaxisdisplayoptions): 
    AxisDisplayOptions
  [PrimaryYAxisLabelOptions](#cfn-quicksight-template-waterfallchartconfiguration-primaryyaxislabeloptions): 
    ChartAxisLabelOptions
  [SortConfiguration](#cfn-quicksight-template-waterfallchartconfiguration-sortconfiguration): 
    WaterfallChartSortConfiguration
  [VisualPalette](#cfn-quicksight-template-waterfallchartconfiguration-visualpalette): 
    VisualPalette
  [WaterfallChartOptions](#cfn-quicksight-template-waterfallchartconfiguration-waterfallchartoptions): 
    WaterfallChartOptions
```

## Properties<a name="aws-properties-quicksight-template-waterfallchartconfiguration-properties"></a>

`CategoryAxisDisplayOptions`  <a name="cfn-quicksight-template-waterfallchartconfiguration-categoryaxisdisplayoptions"></a>
The options that determine the presentation of the category axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-template-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxisLabelOptions`  <a name="cfn-quicksight-template-waterfallchartconfiguration-categoryaxislabeloptions"></a>
The options that determine the presentation of the category axis label\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-template-waterfallchartconfiguration-datalabels"></a>
The data label configuration of a waterfall visual\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-template-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-waterfallchartconfiguration-fieldwells"></a>
The field well configuration of a waterfall visual\.  
*Required*: No  
*Type*: [WaterfallChartFieldWells](aws-properties-quicksight-template-waterfallchartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-template-waterfallchartconfiguration-legend"></a>
The legend configuration of a waterfall visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-template-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisDisplayOptions`  <a name="cfn-quicksight-template-waterfallchartconfiguration-primaryyaxisdisplayoptions"></a>
The options that determine the presentation of the y\-axis\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-template-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryYAxisLabelOptions`  <a name="cfn-quicksight-template-waterfallchartconfiguration-primaryyaxislabeloptions"></a>
The options that determine the presentation of the y\-axis label\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-template-waterfallchartconfiguration-sortconfiguration"></a>
The sort configuration of a waterfall visual\.  
*Required*: No  
*Type*: [WaterfallChartSortConfiguration](aws-properties-quicksight-template-waterfallchartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-template-waterfallchartconfiguration-visualpalette"></a>
The visual palette configuration of a waterfall visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-template-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaterfallChartOptions`  <a name="cfn-quicksight-template-waterfallchartconfiguration-waterfallchartoptions"></a>
The options that determine the presentation of a waterfall visual\.  
*Required*: No  
*Type*: [WaterfallChartOptions](aws-properties-quicksight-template-waterfallchartoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)