# AWS::QuickSight::Dashboard Visual<a name="aws-properties-quicksight-dashboard-visual"></a>

A visual displayed on a sheet in an analysis, dashboard, or template\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-visual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-visual-syntax.json"></a>

```
{
  "[BarChartVisual](#cfn-quicksight-dashboard-visual-barchartvisual)" : BarChartVisual,
  "[BoxPlotVisual](#cfn-quicksight-dashboard-visual-boxplotvisual)" : BoxPlotVisual,
  "[ComboChartVisual](#cfn-quicksight-dashboard-visual-combochartvisual)" : ComboChartVisual,
  "[CustomContentVisual](#cfn-quicksight-dashboard-visual-customcontentvisual)" : CustomContentVisual,
  "[EmptyVisual](#cfn-quicksight-dashboard-visual-emptyvisual)" : EmptyVisual,
  "[FilledMapVisual](#cfn-quicksight-dashboard-visual-filledmapvisual)" : FilledMapVisual,
  "[FunnelChartVisual](#cfn-quicksight-dashboard-visual-funnelchartvisual)" : FunnelChartVisual,
  "[GaugeChartVisual](#cfn-quicksight-dashboard-visual-gaugechartvisual)" : GaugeChartVisual,
  "[GeospatialMapVisual](#cfn-quicksight-dashboard-visual-geospatialmapvisual)" : GeospatialMapVisual,
  "[HeatMapVisual](#cfn-quicksight-dashboard-visual-heatmapvisual)" : HeatMapVisual,
  "[HistogramVisual](#cfn-quicksight-dashboard-visual-histogramvisual)" : HistogramVisual,
  "[InsightVisual](#cfn-quicksight-dashboard-visual-insightvisual)" : InsightVisual,
  "[KPIVisual](#cfn-quicksight-dashboard-visual-kpivisual)" : KPIVisual,
  "[LineChartVisual](#cfn-quicksight-dashboard-visual-linechartvisual)" : LineChartVisual,
  "[PieChartVisual](#cfn-quicksight-dashboard-visual-piechartvisual)" : PieChartVisual,
  "[PivotTableVisual](#cfn-quicksight-dashboard-visual-pivottablevisual)" : PivotTableVisual,
  "[RadarChartVisual](#cfn-quicksight-dashboard-visual-radarchartvisual)" : RadarChartVisual,
  "[SankeyDiagramVisual](#cfn-quicksight-dashboard-visual-sankeydiagramvisual)" : SankeyDiagramVisual,
  "[ScatterPlotVisual](#cfn-quicksight-dashboard-visual-scatterplotvisual)" : ScatterPlotVisual,
  "[TableVisual](#cfn-quicksight-dashboard-visual-tablevisual)" : TableVisual,
  "[TreeMapVisual](#cfn-quicksight-dashboard-visual-treemapvisual)" : TreeMapVisual,
  "[WaterfallVisual](#cfn-quicksight-dashboard-visual-waterfallvisual)" : WaterfallVisual,
  "[WordCloudVisual](#cfn-quicksight-dashboard-visual-wordcloudvisual)" : WordCloudVisual
}
```

### YAML<a name="aws-properties-quicksight-dashboard-visual-syntax.yaml"></a>

```
  [BarChartVisual](#cfn-quicksight-dashboard-visual-barchartvisual): 
    BarChartVisual
  [BoxPlotVisual](#cfn-quicksight-dashboard-visual-boxplotvisual): 
    BoxPlotVisual
  [ComboChartVisual](#cfn-quicksight-dashboard-visual-combochartvisual): 
    ComboChartVisual
  [CustomContentVisual](#cfn-quicksight-dashboard-visual-customcontentvisual): 
    CustomContentVisual
  [EmptyVisual](#cfn-quicksight-dashboard-visual-emptyvisual): 
    EmptyVisual
  [FilledMapVisual](#cfn-quicksight-dashboard-visual-filledmapvisual): 
    FilledMapVisual
  [FunnelChartVisual](#cfn-quicksight-dashboard-visual-funnelchartvisual): 
    FunnelChartVisual
  [GaugeChartVisual](#cfn-quicksight-dashboard-visual-gaugechartvisual): 
    GaugeChartVisual
  [GeospatialMapVisual](#cfn-quicksight-dashboard-visual-geospatialmapvisual): 
    GeospatialMapVisual
  [HeatMapVisual](#cfn-quicksight-dashboard-visual-heatmapvisual): 
    HeatMapVisual
  [HistogramVisual](#cfn-quicksight-dashboard-visual-histogramvisual): 
    HistogramVisual
  [InsightVisual](#cfn-quicksight-dashboard-visual-insightvisual): 
    InsightVisual
  [KPIVisual](#cfn-quicksight-dashboard-visual-kpivisual): 
    KPIVisual
  [LineChartVisual](#cfn-quicksight-dashboard-visual-linechartvisual): 
    LineChartVisual
  [PieChartVisual](#cfn-quicksight-dashboard-visual-piechartvisual): 
    PieChartVisual
  [PivotTableVisual](#cfn-quicksight-dashboard-visual-pivottablevisual): 
    PivotTableVisual
  [RadarChartVisual](#cfn-quicksight-dashboard-visual-radarchartvisual): 
    RadarChartVisual
  [SankeyDiagramVisual](#cfn-quicksight-dashboard-visual-sankeydiagramvisual): 
    SankeyDiagramVisual
  [ScatterPlotVisual](#cfn-quicksight-dashboard-visual-scatterplotvisual): 
    ScatterPlotVisual
  [TableVisual](#cfn-quicksight-dashboard-visual-tablevisual): 
    TableVisual
  [TreeMapVisual](#cfn-quicksight-dashboard-visual-treemapvisual): 
    TreeMapVisual
  [WaterfallVisual](#cfn-quicksight-dashboard-visual-waterfallvisual): 
    WaterfallVisual
  [WordCloudVisual](#cfn-quicksight-dashboard-visual-wordcloudvisual): 
    WordCloudVisual
```

## Properties<a name="aws-properties-quicksight-dashboard-visual-properties"></a>

`BarChartVisual`  <a name="cfn-quicksight-dashboard-visual-barchartvisual"></a>
A bar chart\.  
For more information, see [Using bar charts](https://docs.aws.amazon.com/quicksight/latest/user/bar-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [BarChartVisual](aws-properties-quicksight-dashboard-barchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BoxPlotVisual`  <a name="cfn-quicksight-dashboard-visual-boxplotvisual"></a>
A box plot\.  
For more information, see [Using box plots](https://docs.aws.amazon.com/quicksight/latest/user/box-plots.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [BoxPlotVisual](aws-properties-quicksight-dashboard-boxplotvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComboChartVisual`  <a name="cfn-quicksight-dashboard-visual-combochartvisual"></a>
A combo chart\.  
For more information, see [Using combo charts](https://docs.aws.amazon.com/quicksight/latest/user/combo-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [ComboChartVisual](aws-properties-quicksight-dashboard-combochartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomContentVisual`  <a name="cfn-quicksight-dashboard-visual-customcontentvisual"></a>
A visual that contains custom content\.  
For more information, see [Using custom visual content](https://docs.aws.amazon.com/quicksight/latest/user/custom-visual-content.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [CustomContentVisual](aws-properties-quicksight-dashboard-customcontentvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmptyVisual`  <a name="cfn-quicksight-dashboard-visual-emptyvisual"></a>
An empty visual\.  
*Required*: No  
*Type*: [EmptyVisual](aws-properties-quicksight-dashboard-emptyvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilledMapVisual`  <a name="cfn-quicksight-dashboard-visual-filledmapvisual"></a>
A filled map\.  
For more information, see [Creating filled maps](https://docs.aws.amazon.com/quicksight/latest/user/filled-maps.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [FilledMapVisual](aws-properties-quicksight-dashboard-filledmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunnelChartVisual`  <a name="cfn-quicksight-dashboard-visual-funnelchartvisual"></a>
A funnel chart\.  
For more information, see [Using funnel charts](https://docs.aws.amazon.com/quicksight/latest/user/funnel-visual-content.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [FunnelChartVisual](aws-properties-quicksight-dashboard-funnelchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GaugeChartVisual`  <a name="cfn-quicksight-dashboard-visual-gaugechartvisual"></a>
A gauge chart\.  
For more information, see [Using gauge charts](https://docs.aws.amazon.com/quicksight/latest/user/gauge-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [GaugeChartVisual](aws-properties-quicksight-dashboard-gaugechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeospatialMapVisual`  <a name="cfn-quicksight-dashboard-visual-geospatialmapvisual"></a>
A geospatial map or a points on map visual\.  
For more information, see [Creating point maps](https://docs.aws.amazon.com/quicksight/latest/user/point-maps.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [GeospatialMapVisual](aws-properties-quicksight-dashboard-geospatialmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapVisual`  <a name="cfn-quicksight-dashboard-visual-heatmapvisual"></a>
A heat map\.  
For more information, see [Using heat maps](https://docs.aws.amazon.com/quicksight/latest/user/heat-map.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [HeatMapVisual](aws-properties-quicksight-dashboard-heatmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HistogramVisual`  <a name="cfn-quicksight-dashboard-visual-histogramvisual"></a>
A histogram\.  
For more information, see [Using histograms](https://docs.aws.amazon.com/quicksight/latest/user/histogram-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [HistogramVisual](aws-properties-quicksight-dashboard-histogramvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsightVisual`  <a name="cfn-quicksight-dashboard-visual-insightvisual"></a>
An insight visual\.  
For more information, see [Working with insights](https://docs.aws.amazon.com/quicksight/latest/user/computational-insights.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [InsightVisual](aws-properties-quicksight-dashboard-insightvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KPIVisual`  <a name="cfn-quicksight-dashboard-visual-kpivisual"></a>
A key performance indicator \(KPI\)\.  
For more information, see [Using KPIs](https://docs.aws.amazon.com/quicksight/latest/user/kpi.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [KPIVisual](aws-properties-quicksight-dashboard-kpivisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineChartVisual`  <a name="cfn-quicksight-dashboard-visual-linechartvisual"></a>
A line chart\.  
For more information, see [Using line charts](https://docs.aws.amazon.com/quicksight/latest/user/line-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [LineChartVisual](aws-properties-quicksight-dashboard-linechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PieChartVisual`  <a name="cfn-quicksight-dashboard-visual-piechartvisual"></a>
A pie or donut chart\.  
For more information, see [Using pie charts](https://docs.aws.amazon.com/quicksight/latest/user/pie-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [PieChartVisual](aws-properties-quicksight-dashboard-piechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PivotTableVisual`  <a name="cfn-quicksight-dashboard-visual-pivottablevisual"></a>
A pivot table\.  
For more information, see [Using pivot tables](https://docs.aws.amazon.com/quicksight/latest/user/pivot-table.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [PivotTableVisual](aws-properties-quicksight-dashboard-pivottablevisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RadarChartVisual`  <a name="cfn-quicksight-dashboard-visual-radarchartvisual"></a>
A radar chart visual\.  
For more information, see [Using radar charts](https://docs.aws.amazon.com/quicksight/latest/user/radar-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [RadarChartVisual](aws-properties-quicksight-dashboard-radarchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SankeyDiagramVisual`  <a name="cfn-quicksight-dashboard-visual-sankeydiagramvisual"></a>
A sankey diagram\.  
For more information, see [Using Sankey diagrams](https://docs.aws.amazon.com/quicksight/latest/user/sankey-diagram.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [SankeyDiagramVisual](aws-properties-quicksight-dashboard-sankeydiagramvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScatterPlotVisual`  <a name="cfn-quicksight-dashboard-visual-scatterplotvisual"></a>
A scatter plot\.  
For more information, see [Using scatter plots](https://docs.aws.amazon.com/quicksight/latest/user/scatter-plot.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [ScatterPlotVisual](aws-properties-quicksight-dashboard-scatterplotvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableVisual`  <a name="cfn-quicksight-dashboard-visual-tablevisual"></a>
A table visual\.  
For more information, see [Using tables as visuals](https://docs.aws.amazon.com/quicksight/latest/user/tabular.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [TableVisual](aws-properties-quicksight-dashboard-tablevisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreeMapVisual`  <a name="cfn-quicksight-dashboard-visual-treemapvisual"></a>
A tree map\.  
For more information, see [Using tree maps](https://docs.aws.amazon.com/quicksight/latest/user/tree-map.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [TreeMapVisual](aws-properties-quicksight-dashboard-treemapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaterfallVisual`  <a name="cfn-quicksight-dashboard-visual-waterfallvisual"></a>
A waterfall chart\.  
For more information, see [Using waterfall charts](https://docs.aws.amazon.com/quicksight/latest/user/waterfall-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [WaterfallVisual](aws-properties-quicksight-dashboard-waterfallvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WordCloudVisual`  <a name="cfn-quicksight-dashboard-visual-wordcloudvisual"></a>
A word cloud\.  
For more information, see [Using word clouds](https://docs.aws.amazon.com/quicksight/latest/user/word-cloud.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [WordCloudVisual](aws-properties-quicksight-dashboard-wordcloudvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)