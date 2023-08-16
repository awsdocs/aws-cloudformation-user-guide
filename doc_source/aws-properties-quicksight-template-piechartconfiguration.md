# AWS::QuickSight::Template PieChartConfiguration<a name="aws-properties-quicksight-template-piechartconfiguration"></a>

The configuration of a pie chart\.

## Syntax<a name="aws-properties-quicksight-template-piechartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-piechartconfiguration-syntax.json"></a>

```
{
  "[CategoryLabelOptions](#cfn-quicksight-template-piechartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[ContributionAnalysisDefaults](#cfn-quicksight-template-piechartconfiguration-contributionanalysisdefaults)" : [ ContributionAnalysisDefault, ... ],
  "[DataLabels](#cfn-quicksight-template-piechartconfiguration-datalabels)" : DataLabelOptions,
  "[DonutOptions](#cfn-quicksight-template-piechartconfiguration-donutoptions)" : DonutOptions,
  "[FieldWells](#cfn-quicksight-template-piechartconfiguration-fieldwells)" : PieChartFieldWells,
  "[Legend](#cfn-quicksight-template-piechartconfiguration-legend)" : LegendOptions,
  "[SmallMultiplesOptions](#cfn-quicksight-template-piechartconfiguration-smallmultiplesoptions)" : SmallMultiplesOptions,
  "[SortConfiguration](#cfn-quicksight-template-piechartconfiguration-sortconfiguration)" : PieChartSortConfiguration,
  "[Tooltip](#cfn-quicksight-template-piechartconfiguration-tooltip)" : TooltipOptions,
  "[ValueLabelOptions](#cfn-quicksight-template-piechartconfiguration-valuelabeloptions)" : ChartAxisLabelOptions,
  "[VisualPalette](#cfn-quicksight-template-piechartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-template-piechartconfiguration-syntax.yaml"></a>

```
  [CategoryLabelOptions](#cfn-quicksight-template-piechartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [ContributionAnalysisDefaults](#cfn-quicksight-template-piechartconfiguration-contributionanalysisdefaults): 
    - ContributionAnalysisDefault
  [DataLabels](#cfn-quicksight-template-piechartconfiguration-datalabels): 
    DataLabelOptions
  [DonutOptions](#cfn-quicksight-template-piechartconfiguration-donutoptions): 
    DonutOptions
  [FieldWells](#cfn-quicksight-template-piechartconfiguration-fieldwells): 
    PieChartFieldWells
  [Legend](#cfn-quicksight-template-piechartconfiguration-legend): 
    LegendOptions
  [SmallMultiplesOptions](#cfn-quicksight-template-piechartconfiguration-smallmultiplesoptions): 
    SmallMultiplesOptions
  [SortConfiguration](#cfn-quicksight-template-piechartconfiguration-sortconfiguration): 
    PieChartSortConfiguration
  [Tooltip](#cfn-quicksight-template-piechartconfiguration-tooltip): 
    TooltipOptions
  [ValueLabelOptions](#cfn-quicksight-template-piechartconfiguration-valuelabeloptions): 
    ChartAxisLabelOptions
  [VisualPalette](#cfn-quicksight-template-piechartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-template-piechartconfiguration-properties"></a>

`CategoryLabelOptions`  <a name="cfn-quicksight-template-piechartconfiguration-categorylabeloptions"></a>
The label options of the group/color that is displayed in a pie chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContributionAnalysisDefaults`  <a name="cfn-quicksight-template-piechartconfiguration-contributionanalysisdefaults"></a>
The contribution analysis \(anomaly configuration\) setup of the visual\.  
*Required*: No  
*Type*: List of [ContributionAnalysisDefault](aws-properties-quicksight-template-contributionanalysisdefault.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-template-piechartconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-template-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DonutOptions`  <a name="cfn-quicksight-template-piechartconfiguration-donutoptions"></a>
The options that determine the shape of the chart\. This option determines whether the chart is a pie chart or a donut chart\.  
*Required*: No  
*Type*: [DonutOptions](aws-properties-quicksight-template-donutoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-piechartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [PieChartFieldWells](aws-properties-quicksight-template-piechartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-template-piechartconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-template-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesOptions`  <a name="cfn-quicksight-template-piechartconfiguration-smallmultiplesoptions"></a>
The small multiples setup for the visual\.  
*Required*: No  
*Type*: [SmallMultiplesOptions](aws-properties-quicksight-template-smallmultiplesoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-template-piechartconfiguration-sortconfiguration"></a>
The sort configuration of a pie chart\.  
*Required*: No  
*Type*: [PieChartSortConfiguration](aws-properties-quicksight-template-piechartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-template-piechartconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-template-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueLabelOptions`  <a name="cfn-quicksight-template-piechartconfiguration-valuelabeloptions"></a>
The label options for the value that is displayed in a pie chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-template-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-template-piechartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-template-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)