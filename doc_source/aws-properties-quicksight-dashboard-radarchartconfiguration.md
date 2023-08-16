# AWS::QuickSight::Dashboard RadarChartConfiguration<a name="aws-properties-quicksight-dashboard-radarchartconfiguration"></a>

The configuration of a `RadarChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-radarchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-radarchartconfiguration-syntax.json"></a>

```
{
  "[AlternateBandColorsVisibility](#cfn-quicksight-dashboard-radarchartconfiguration-alternatebandcolorsvisibility)" : String,
  "[AlternateBandEvenColor](#cfn-quicksight-dashboard-radarchartconfiguration-alternatebandevencolor)" : String,
  "[AlternateBandOddColor](#cfn-quicksight-dashboard-radarchartconfiguration-alternatebandoddcolor)" : String,
  "[AxesRangeScale](#cfn-quicksight-dashboard-radarchartconfiguration-axesrangescale)" : String,
  "[BaseSeriesSettings](#cfn-quicksight-dashboard-radarchartconfiguration-baseseriessettings)" : RadarChartSeriesSettings,
  "[CategoryAxis](#cfn-quicksight-dashboard-radarchartconfiguration-categoryaxis)" : AxisDisplayOptions,
  "[CategoryLabelOptions](#cfn-quicksight-dashboard-radarchartconfiguration-categorylabeloptions)" : ChartAxisLabelOptions,
  "[ColorAxis](#cfn-quicksight-dashboard-radarchartconfiguration-coloraxis)" : AxisDisplayOptions,
  "[ColorLabelOptions](#cfn-quicksight-dashboard-radarchartconfiguration-colorlabeloptions)" : ChartAxisLabelOptions,
  "[FieldWells](#cfn-quicksight-dashboard-radarchartconfiguration-fieldwells)" : RadarChartFieldWells,
  "[Legend](#cfn-quicksight-dashboard-radarchartconfiguration-legend)" : LegendOptions,
  "[Shape](#cfn-quicksight-dashboard-radarchartconfiguration-shape)" : String,
  "[SortConfiguration](#cfn-quicksight-dashboard-radarchartconfiguration-sortconfiguration)" : RadarChartSortConfiguration,
  "[StartAngle](#cfn-quicksight-dashboard-radarchartconfiguration-startangle)" : Double,
  "[VisualPalette](#cfn-quicksight-dashboard-radarchartconfiguration-visualpalette)" : VisualPalette
}
```

### YAML<a name="aws-properties-quicksight-dashboard-radarchartconfiguration-syntax.yaml"></a>

```
  [AlternateBandColorsVisibility](#cfn-quicksight-dashboard-radarchartconfiguration-alternatebandcolorsvisibility): String
  [AlternateBandEvenColor](#cfn-quicksight-dashboard-radarchartconfiguration-alternatebandevencolor): String
  [AlternateBandOddColor](#cfn-quicksight-dashboard-radarchartconfiguration-alternatebandoddcolor): String
  [AxesRangeScale](#cfn-quicksight-dashboard-radarchartconfiguration-axesrangescale): String
  [BaseSeriesSettings](#cfn-quicksight-dashboard-radarchartconfiguration-baseseriessettings): 
    RadarChartSeriesSettings
  [CategoryAxis](#cfn-quicksight-dashboard-radarchartconfiguration-categoryaxis): 
    AxisDisplayOptions
  [CategoryLabelOptions](#cfn-quicksight-dashboard-radarchartconfiguration-categorylabeloptions): 
    ChartAxisLabelOptions
  [ColorAxis](#cfn-quicksight-dashboard-radarchartconfiguration-coloraxis): 
    AxisDisplayOptions
  [ColorLabelOptions](#cfn-quicksight-dashboard-radarchartconfiguration-colorlabeloptions): 
    ChartAxisLabelOptions
  [FieldWells](#cfn-quicksight-dashboard-radarchartconfiguration-fieldwells): 
    RadarChartFieldWells
  [Legend](#cfn-quicksight-dashboard-radarchartconfiguration-legend): 
    LegendOptions
  [Shape](#cfn-quicksight-dashboard-radarchartconfiguration-shape): String
  [SortConfiguration](#cfn-quicksight-dashboard-radarchartconfiguration-sortconfiguration): 
    RadarChartSortConfiguration
  [StartAngle](#cfn-quicksight-dashboard-radarchartconfiguration-startangle): Double
  [VisualPalette](#cfn-quicksight-dashboard-radarchartconfiguration-visualpalette): 
    VisualPalette
```

## Properties<a name="aws-properties-quicksight-dashboard-radarchartconfiguration-properties"></a>

`AlternateBandColorsVisibility`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-alternatebandcolorsvisibility"></a>
Determines the visibility of the colors of alternatign bands in a radar chart\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlternateBandEvenColor`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-alternatebandevencolor"></a>
The color of the even\-numbered alternate bands of a radar chart\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlternateBandOddColor`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-alternatebandoddcolor"></a>
The color of the odd\-numbered alternate bands of a radar chart\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AxesRangeScale`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-axesrangescale"></a>
The axis behavior options of a radar chart\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | INDEPENDENT | SHARED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaseSeriesSettings`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-baseseriessettings"></a>
The base sreies settings of a radar chart\.  
*Required*: No  
*Type*: [RadarChartSeriesSettings](aws-properties-quicksight-dashboard-radarchartseriessettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryAxis`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-categoryaxis"></a>
The category axis of a radar chart\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryLabelOptions`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-categorylabeloptions"></a>
The category label options of a radar chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorAxis`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-coloraxis"></a>
The color axis of a radar chart\.  
*Required*: No  
*Type*: [AxisDisplayOptions](aws-properties-quicksight-dashboard-axisdisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorLabelOptions`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-colorlabeloptions"></a>
The color label options of a radar chart\.  
*Required*: No  
*Type*: [ChartAxisLabelOptions](aws-properties-quicksight-dashboard-chartaxislabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-fieldwells"></a>
The field well configuration of a `RadarChartVisual`\.  
*Required*: No  
*Type*: [RadarChartFieldWells](aws-properties-quicksight-dashboard-radarchartfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Shape`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-shape"></a>
The shape of the radar chart\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CIRCLE | POLYGON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-sortconfiguration"></a>
The sort configuration of a `RadarChartVisual`\.  
*Required*: No  
*Type*: [RadarChartSortConfiguration](aws-properties-quicksight-dashboard-radarchartsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartAngle`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-startangle"></a>
The start angle of a radar chart's axis\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-dashboard-radarchartconfiguration-visualpalette"></a>
The palette \(chart color\) display setup of the visual\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-dashboard-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)