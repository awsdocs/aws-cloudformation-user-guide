# AWS::QuickSight::Analysis Visual<a name="aws-properties-quicksight-analysis-visual"></a>

A visual displayed on a sheet in an analysis, dashboard, or template\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-visual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-visual-syntax.json"></a>

```
{
  "[BarChartVisual](#cfn-quicksight-analysis-visual-barchartvisual)" : BarChartVisual,
  "[BoxPlotVisual](#cfn-quicksight-analysis-visual-boxplotvisual)" : BoxPlotVisual,
  "[ComboChartVisual](#cfn-quicksight-analysis-visual-combochartvisual)" : ComboChartVisual,
  "[CustomContentVisual](#cfn-quicksight-analysis-visual-customcontentvisual)" : CustomContentVisual,
  "[EmptyVisual](#cfn-quicksight-analysis-visual-emptyvisual)" : EmptyVisual,
  "[FilledMapVisual](#cfn-quicksight-analysis-visual-filledmapvisual)" : FilledMapVisual,
  "[FunnelChartVisual](#cfn-quicksight-analysis-visual-funnelchartvisual)" : FunnelChartVisual,
  "[GaugeChartVisual](#cfn-quicksight-analysis-visual-gaugechartvisual)" : GaugeChartVisual,
  "[GeospatialMapVisual](#cfn-quicksight-analysis-visual-geospatialmapvisual)" : GeospatialMapVisual,
  "[HeatMapVisual](#cfn-quicksight-analysis-visual-heatmapvisual)" : HeatMapVisual,
  "[HistogramVisual](#cfn-quicksight-analysis-visual-histogramvisual)" : HistogramVisual,
  "[InsightVisual](#cfn-quicksight-analysis-visual-insightvisual)" : InsightVisual,
  "[KPIVisual](#cfn-quicksight-analysis-visual-kpivisual)" : KPIVisual,
  "[LineChartVisual](#cfn-quicksight-analysis-visual-linechartvisual)" : LineChartVisual,
  "[PieChartVisual](#cfn-quicksight-analysis-visual-piechartvisual)" : PieChartVisual,
  "[PivotTableVisual](#cfn-quicksight-analysis-visual-pivottablevisual)" : PivotTableVisual,
  "[RadarChartVisual](#cfn-quicksight-analysis-visual-radarchartvisual)" : RadarChartVisual,
  "[SankeyDiagramVisual](#cfn-quicksight-analysis-visual-sankeydiagramvisual)" : SankeyDiagramVisual,
  "[ScatterPlotVisual](#cfn-quicksight-analysis-visual-scatterplotvisual)" : ScatterPlotVisual,
  "[TableVisual](#cfn-quicksight-analysis-visual-tablevisual)" : TableVisual,
  "[TreeMapVisual](#cfn-quicksight-analysis-visual-treemapvisual)" : TreeMapVisual,
  "[WaterfallVisual](#cfn-quicksight-analysis-visual-waterfallvisual)" : WaterfallVisual,
  "[WordCloudVisual](#cfn-quicksight-analysis-visual-wordcloudvisual)" : WordCloudVisual
}
```

### YAML<a name="aws-properties-quicksight-analysis-visual-syntax.yaml"></a>

```
  [BarChartVisual](#cfn-quicksight-analysis-visual-barchartvisual): 
    BarChartVisual
  [BoxPlotVisual](#cfn-quicksight-analysis-visual-boxplotvisual): 
    BoxPlotVisual
  [ComboChartVisual](#cfn-quicksight-analysis-visual-combochartvisual): 
    ComboChartVisual
  [CustomContentVisual](#cfn-quicksight-analysis-visual-customcontentvisual): 
    CustomContentVisual
  [EmptyVisual](#cfn-quicksight-analysis-visual-emptyvisual): 
    EmptyVisual
  [FilledMapVisual](#cfn-quicksight-analysis-visual-filledmapvisual): 
    FilledMapVisual
  [FunnelChartVisual](#cfn-quicksight-analysis-visual-funnelchartvisual): 
    FunnelChartVisual
  [GaugeChartVisual](#cfn-quicksight-analysis-visual-gaugechartvisual): 
    GaugeChartVisual
  [GeospatialMapVisual](#cfn-quicksight-analysis-visual-geospatialmapvisual): 
    GeospatialMapVisual
  [HeatMapVisual](#cfn-quicksight-analysis-visual-heatmapvisual): 
    HeatMapVisual
  [HistogramVisual](#cfn-quicksight-analysis-visual-histogramvisual): 
    HistogramVisual
  [InsightVisual](#cfn-quicksight-analysis-visual-insightvisual): 
    InsightVisual
  [KPIVisual](#cfn-quicksight-analysis-visual-kpivisual): 
    KPIVisual
  [LineChartVisual](#cfn-quicksight-analysis-visual-linechartvisual): 
    LineChartVisual
  [PieChartVisual](#cfn-quicksight-analysis-visual-piechartvisual): 
    PieChartVisual
  [PivotTableVisual](#cfn-quicksight-analysis-visual-pivottablevisual): 
    PivotTableVisual
  [RadarChartVisual](#cfn-quicksight-analysis-visual-radarchartvisual): 
    RadarChartVisual
  [SankeyDiagramVisual](#cfn-quicksight-analysis-visual-sankeydiagramvisual): 
    SankeyDiagramVisual
  [ScatterPlotVisual](#cfn-quicksight-analysis-visual-scatterplotvisual): 
    ScatterPlotVisual
  [TableVisual](#cfn-quicksight-analysis-visual-tablevisual): 
    TableVisual
  [TreeMapVisual](#cfn-quicksight-analysis-visual-treemapvisual): 
    TreeMapVisual
  [WaterfallVisual](#cfn-quicksight-analysis-visual-waterfallvisual): 
    WaterfallVisual
  [WordCloudVisual](#cfn-quicksight-analysis-visual-wordcloudvisual): 
    WordCloudVisual
```

## Properties<a name="aws-properties-quicksight-analysis-visual-properties"></a>

`BarChartVisual`  <a name="cfn-quicksight-analysis-visual-barchartvisual"></a>
A bar chart\.  
For more information, see [Using bar charts](https://docs.aws.amazon.com/quicksight/latest/user/bar-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [BarChartVisual](aws-properties-quicksight-analysis-barchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BoxPlotVisual`  <a name="cfn-quicksight-analysis-visual-boxplotvisual"></a>
A box plot\.  
For more information, see [Using box plots](https://docs.aws.amazon.com/quicksight/latest/user/box-plots.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [BoxPlotVisual](aws-properties-quicksight-analysis-boxplotvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComboChartVisual`  <a name="cfn-quicksight-analysis-visual-combochartvisual"></a>
A combo chart\.  
For more information, see [Using combo charts](https://docs.aws.amazon.com/quicksight/latest/user/combo-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [ComboChartVisual](aws-properties-quicksight-analysis-combochartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomContentVisual`  <a name="cfn-quicksight-analysis-visual-customcontentvisual"></a>
A visual that contains custom content\.  
For more information, see [Using custom visual content](https://docs.aws.amazon.com/quicksight/latest/user/custom-visual-content.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [CustomContentVisual](aws-properties-quicksight-analysis-customcontentvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmptyVisual`  <a name="cfn-quicksight-analysis-visual-emptyvisual"></a>
An empty visual\.  
*Required*: No  
*Type*: [EmptyVisual](aws-properties-quicksight-analysis-emptyvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilledMapVisual`  <a name="cfn-quicksight-analysis-visual-filledmapvisual"></a>
A filled map\.  
For more information, see [Creating filled maps](https://docs.aws.amazon.com/quicksight/latest/user/filled-maps.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [FilledMapVisual](aws-properties-quicksight-analysis-filledmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunnelChartVisual`  <a name="cfn-quicksight-analysis-visual-funnelchartvisual"></a>
A funnel chart\.  
For more information, see [Using funnel charts](https://docs.aws.amazon.com/quicksight/latest/user/funnel-visual-content.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [FunnelChartVisual](aws-properties-quicksight-analysis-funnelchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GaugeChartVisual`  <a name="cfn-quicksight-analysis-visual-gaugechartvisual"></a>
A gauge chart\.  
For more information, see [Using gauge charts](https://docs.aws.amazon.com/quicksight/latest/user/gauge-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [GaugeChartVisual](aws-properties-quicksight-analysis-gaugechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeospatialMapVisual`  <a name="cfn-quicksight-analysis-visual-geospatialmapvisual"></a>
A geospatial map or a points on map visual\.  
For more information, see [Creating point maps](https://docs.aws.amazon.com/quicksight/latest/user/point-maps.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [GeospatialMapVisual](aws-properties-quicksight-analysis-geospatialmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapVisual`  <a name="cfn-quicksight-analysis-visual-heatmapvisual"></a>
A heat map\.  
For more information, see [Using heat maps](https://docs.aws.amazon.com/quicksight/latest/user/heat-map.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [HeatMapVisual](aws-properties-quicksight-analysis-heatmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HistogramVisual`  <a name="cfn-quicksight-analysis-visual-histogramvisual"></a>
A histogram\.  
For more information, see [Using histograms](https://docs.aws.amazon.com/quicksight/latest/user/histogram-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [HistogramVisual](aws-properties-quicksight-analysis-histogramvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsightVisual`  <a name="cfn-quicksight-analysis-visual-insightvisual"></a>
An insight visual\.  
For more information, see [Working with insights](https://docs.aws.amazon.com/quicksight/latest/user/computational-insights.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [InsightVisual](aws-properties-quicksight-analysis-insightvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KPIVisual`  <a name="cfn-quicksight-analysis-visual-kpivisual"></a>
A key performance indicator \(KPI\)\.  
For more information, see [Using KPIs](https://docs.aws.amazon.com/quicksight/latest/user/kpi.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [KPIVisual](aws-properties-quicksight-analysis-kpivisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineChartVisual`  <a name="cfn-quicksight-analysis-visual-linechartvisual"></a>
A line chart\.  
For more information, see [Using line charts](https://docs.aws.amazon.com/quicksight/latest/user/line-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [LineChartVisual](aws-properties-quicksight-analysis-linechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PieChartVisual`  <a name="cfn-quicksight-analysis-visual-piechartvisual"></a>
A pie or donut chart\.  
For more information, see [Using pie charts](https://docs.aws.amazon.com/quicksight/latest/user/pie-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [PieChartVisual](aws-properties-quicksight-analysis-piechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PivotTableVisual`  <a name="cfn-quicksight-analysis-visual-pivottablevisual"></a>
A pivot table\.  
For more information, see [Using pivot tables](https://docs.aws.amazon.com/quicksight/latest/user/pivot-table.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [PivotTableVisual](aws-properties-quicksight-analysis-pivottablevisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RadarChartVisual`  <a name="cfn-quicksight-analysis-visual-radarchartvisual"></a>
A radar chart visual\.  
For more information, see [Using radar charts](https://docs.aws.amazon.com/quicksight/latest/user/radar-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [RadarChartVisual](aws-properties-quicksight-analysis-radarchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SankeyDiagramVisual`  <a name="cfn-quicksight-analysis-visual-sankeydiagramvisual"></a>
A sankey diagram\.  
For more information, see [Using Sankey diagrams](https://docs.aws.amazon.com/quicksight/latest/user/sankey-diagram.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [SankeyDiagramVisual](aws-properties-quicksight-analysis-sankeydiagramvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScatterPlotVisual`  <a name="cfn-quicksight-analysis-visual-scatterplotvisual"></a>
A scatter plot\.  
For more information, see [Using scatter plots](https://docs.aws.amazon.com/quicksight/latest/user/scatter-plot.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [ScatterPlotVisual](aws-properties-quicksight-analysis-scatterplotvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableVisual`  <a name="cfn-quicksight-analysis-visual-tablevisual"></a>
A table visual\.  
For more information, see [Using tables as visuals](https://docs.aws.amazon.com/quicksight/latest/user/tabular.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [TableVisual](aws-properties-quicksight-analysis-tablevisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreeMapVisual`  <a name="cfn-quicksight-analysis-visual-treemapvisual"></a>
A tree map\.  
For more information, see [Using tree maps](https://docs.aws.amazon.com/quicksight/latest/user/tree-map.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [TreeMapVisual](aws-properties-quicksight-analysis-treemapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaterfallVisual`  <a name="cfn-quicksight-analysis-visual-waterfallvisual"></a>
A waterfall chart\.  
For more information, see [Using waterfall charts](https://docs.aws.amazon.com/quicksight/latest/user/waterfall-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [WaterfallVisual](aws-properties-quicksight-analysis-waterfallvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WordCloudVisual`  <a name="cfn-quicksight-analysis-visual-wordcloudvisual"></a>
A word cloud\.  
For more information, see [Using word clouds](https://docs.aws.amazon.com/quicksight/latest/user/word-cloud.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [WordCloudVisual](aws-properties-quicksight-analysis-wordcloudvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)