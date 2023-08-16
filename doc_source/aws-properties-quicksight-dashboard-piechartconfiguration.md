# AWS::QuickSight::Dashboard PieChartConfiguration<a name="aws-properties-quicksight-dashboard-piechartconfiguration"></a>

The configuration of a pie chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-piechartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-piechartconfiguration-syntax.json"></a>

```
{
  "[CategoryLabelOptions](#cfn-quicksight-dashboard-piechartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[ContributionAnalysisDefaults](#cfn-quicksight-dashboard-piechartconfiguration-contributionanalysisdefaults)" : [ ContributionAnalysisDefault, ... ],
  "[DataLabels](#cfn-quicksight-dashboard-piechartconfiguration-datalabels)" : DataLabelOptions,
  "[DonutOptions](#cfn-quicksight-dashboard-piechartconfiguration-donutoptions)" : DonutOptions,
  "[FieldWells](#cfn-quicksight-dashboard-piechartconfiguration-fieldwells)" : PieChartFieldWells,
  "[Legend](#cfn-quicksight-dashboard-piechartconfiguration-legend)" : LegendOptions,
  "[SmallMultiplesOptions](#cfn-quicksight-dashboard-piechartconfiguration-smallmultiplesoptions)" : SmallMultiplesOptions,
  "[SortConfiguration](#cfn-quicksight-dashboard-piechartconfiguration-sortconfiguration)" : PieChartSortConfiguration,
  "[Tooltip](#cfn-quicksight-dashboard-piechartconfiguration-tooltip)" : TooltipOptions,
  "[ValueLabelOptions](#cfn-quicksight-dashboard-piechartconfiguration-valuelabeloptions)" : ChartAxisLabelOptions,
  "[VisualPalette](#cfn-quicksight-dashboard-piechartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-dashboard-piechartconfiguration-syntax.yaml"></a>

```
  [CategoryLabelOptions](#cfn-quicksight-dashboard-piechartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [ContributionAnalysisDefaults](#cfn-quicksight-dashboard-piechartconfiguration-contributionanalysisdefaults): 
    - ContributionAnalysisDefault
  [DataLabels](#cfn-quicksight-dashboard-piechartconfiguration-datalabels): 
    DataLabelOptions
  [DonutOptions](#cfn-quicksight-dashboard-piechartconfiguration-donutoptions): 
    DonutOptions
  [FieldWells](#cfn-quicksight-dashboard-piechartconfiguration-fieldwells): 
    PieChartFieldWells
  [Legend](#cfn-quicksight-dashboard-piechartconfiguration-legend): 
    LegendOptions
  [SmallMultiplesOptions](#cfn-quicksight-dashboard-piechartconfiguration-smallmultiplesoptions): 
    SmallMultiplesOptions
  [SortConfiguration](#cfn-quicksight-dashboard-piechartconfiguration-sortconfiguration): 
    PieChartSortConfiguration
  [Tooltip](#cfn-quicksight-dashboard-piechartconfiguration-tooltip): 
    TooltipOptions
  [ValueLabelOptions](#cfn-quicksight-dashboard-piechartconfiguration-valuelabeloptions): 
    ChartAxisLabelOptions
  [VisualPalette](#cfn-quicksight-dashboard-piechartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-dashboard-piechartconfiguration-properties"></a>

`CategoryLabelOptions`  <a name="cfn-quicksight-dashboard-piechartconfiguration-categorylabeloptions"></a>
The label options of the group/color that is displayed in a pie chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContributionAnalysisDefaults`  <a name="cfn-quicksight-dashboard-piechartconfiguration-contributionanalysisdefaults"></a>
The contribution analysis \(anomaly configuration\) setup of the visual\.  
*Required*: No  
*Type*: List of [ContributionAnalysisDefault](aws-properties-quicksight-dashboard-contributionanalysisdefault.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabels`  <a name="cfn-quicksight-dashboard-piechartconfiguration-datalabels"></a>
The options that determine if visual data labels are displayed\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-dashboard-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DonutOptions`  <a name="cfn-quicksight-dashboard-piechartconfiguration-donutoptions"></a>
The options that determine the shape of the chart\. This option determines whether the chart is a pie chart or a donut chart\.  
*Required*: No  
*Type*: [DonutOptions](aws-properties-quicksight-dashboard-donutoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-piechartconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [PieChartFieldWells](aws-properties-quicksight-dashboard-piechartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-piechartconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesOptions`  <a name="cfn-quicksight-dashboard-piechartconfiguration-smallmultiplesoptions"></a>
The small multiples setup for the visual\.  
*Required*: No  
*Type*: [SmallMultiplesOptions](aws-properties-quicksight-dashboard-smallmultiplesoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-piechartconfiguration-sortconfiguration"></a>
The sort configuration of a pie chart\.  
*Required*: No  
*Type*: [PieChartSortConfiguration](aws-properties-quicksight-dashboard-piechartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-dashboard-piechartconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-dashboard-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueLabelOptions`  <a name="cfn-quicksight-dashboard-piechartconfiguration-valuelabeloptions"></a>
The label options for the value that is displayed in a pie chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-dashboard-piechartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-dashboard-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)