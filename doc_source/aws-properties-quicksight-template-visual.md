# AWS::QuickSight::Template Visual<a name="aws-properties-quicksight-template-visual"></a>

A visual displayed on a sheet in an analysis, dashboard, or template\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-visual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-visual-syntax.json"></a>

```
{
  "[BarChartVisual](#cfn-quicksight-template-visual-barchartvisual)" : BarChartVisual,
  "[BoxPlotVisual](#cfn-quicksight-template-visual-boxplotvisual)" : BoxPlotVisual,
  "[ComboChartVisual](#cfn-quicksight-template-visual-combochartvisual)" : ComboChartVisual,
  "[CustomContentVisual](#cfn-quicksight-template-visual-customcontentvisual)" : CustomContentVisual,
  "[EmptyVisual](#cfn-quicksight-template-visual-emptyvisual)" : EmptyVisual,
  "[FilledMapVisual](#cfn-quicksight-template-visual-filledmapvisual)" : FilledMapVisual,
  "[FunnelChartVisual](#cfn-quicksight-template-visual-funnelchartvisual)" : FunnelChartVisual,
  "[GaugeChartVisual](#cfn-quicksight-template-visual-gaugechartvisual)" : GaugeChartVisual,
  "[GeospatialMapVisual](#cfn-quicksight-template-visual-geospatialmapvisual)" : GeospatialMapVisual,
  "[HeatMapVisual](#cfn-quicksight-template-visual-heatmapvisual)" : HeatMapVisual,
  "[HistogramVisual](#cfn-quicksight-template-visual-histogramvisual)" : HistogramVisual,
  "[InsightVisual](#cfn-quicksight-template-visual-insightvisual)" : InsightVisual,
  "[KPIVisual](#cfn-quicksight-template-visual-kpivisual)" : KPIVisual,
  "[LineChartVisual](#cfn-quicksight-template-visual-linechartvisual)" : LineChartVisual,
  "[PieChartVisual](#cfn-quicksight-template-visual-piechartvisual)" : PieChartVisual,
  "[PivotTableVisual](#cfn-quicksight-template-visual-pivottablevisual)" : PivotTableVisual,
  "[RadarChartVisual](#cfn-quicksight-template-visual-radarchartvisual)" : RadarChartVisual,
  "[SankeyDiagramVisual](#cfn-quicksight-template-visual-sankeydiagramvisual)" : SankeyDiagramVisual,
  "[ScatterPlotVisual](#cfn-quicksight-template-visual-scatterplotvisual)" : ScatterPlotVisual,
  "[TableVisual](#cfn-quicksight-template-visual-tablevisual)" : TableVisual,
  "[TreeMapVisual](#cfn-quicksight-template-visual-treemapvisual)" : TreeMapVisual,
  "[WaterfallVisual](#cfn-quicksight-template-visual-waterfallvisual)" : WaterfallVisual,
  "[WordCloudVisual](#cfn-quicksight-template-visual-wordcloudvisual)" : WordCloudVisual
}
```

### YAML<a name="aws-properties-quicksight-template-visual-syntax.yaml"></a>

```
  [BarChartVisual](#cfn-quicksight-template-visual-barchartvisual): 
    BarChartVisual
  [BoxPlotVisual](#cfn-quicksight-template-visual-boxplotvisual): 
    BoxPlotVisual
  [ComboChartVisual](#cfn-quicksight-template-visual-combochartvisual): 
    ComboChartVisual
  [CustomContentVisual](#cfn-quicksight-template-visual-customcontentvisual): 
    CustomContentVisual
  [EmptyVisual](#cfn-quicksight-template-visual-emptyvisual): 
    EmptyVisual
  [FilledMapVisual](#cfn-quicksight-template-visual-filledmapvisual): 
    FilledMapVisual
  [FunnelChartVisual](#cfn-quicksight-template-visual-funnelchartvisual): 
    FunnelChartVisual
  [GaugeChartVisual](#cfn-quicksight-template-visual-gaugechartvisual): 
    GaugeChartVisual
  [GeospatialMapVisual](#cfn-quicksight-template-visual-geospatialmapvisual): 
    GeospatialMapVisual
  [HeatMapVisual](#cfn-quicksight-template-visual-heatmapvisual): 
    HeatMapVisual
  [HistogramVisual](#cfn-quicksight-template-visual-histogramvisual): 
    HistogramVisual
  [InsightVisual](#cfn-quicksight-template-visual-insightvisual): 
    InsightVisual
  [KPIVisual](#cfn-quicksight-template-visual-kpivisual): 
    KPIVisual
  [LineChartVisual](#cfn-quicksight-template-visual-linechartvisual): 
    LineChartVisual
  [PieChartVisual](#cfn-quicksight-template-visual-piechartvisual): 
    PieChartVisual
  [PivotTableVisual](#cfn-quicksight-template-visual-pivottablevisual): 
    PivotTableVisual
  [RadarChartVisual](#cfn-quicksight-template-visual-radarchartvisual): 
    RadarChartVisual
  [SankeyDiagramVisual](#cfn-quicksight-template-visual-sankeydiagramvisual): 
    SankeyDiagramVisual
  [ScatterPlotVisual](#cfn-quicksight-template-visual-scatterplotvisual): 
    ScatterPlotVisual
  [TableVisual](#cfn-quicksight-template-visual-tablevisual): 
    TableVisual
  [TreeMapVisual](#cfn-quicksight-template-visual-treemapvisual): 
    TreeMapVisual
  [WaterfallVisual](#cfn-quicksight-template-visual-waterfallvisual): 
    WaterfallVisual
  [WordCloudVisual](#cfn-quicksight-template-visual-wordcloudvisual): 
    WordCloudVisual
```

## Properties<a name="aws-properties-quicksight-template-visual-properties"></a>

`BarChartVisual`  <a name="cfn-quicksight-template-visual-barchartvisual"></a>
A bar chart\.  
For more information, see [Using bar charts](https://docs.aws.amazon.com/quicksight/latest/user/bar-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [BarChartVisual](aws-properties-quicksight-template-barchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BoxPlotVisual`  <a name="cfn-quicksight-template-visual-boxplotvisual"></a>
A box plot\.  
For more information, see [Using box plots](https://docs.aws.amazon.com/quicksight/latest/user/box-plots.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [BoxPlotVisual](aws-properties-quicksight-template-boxplotvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComboChartVisual`  <a name="cfn-quicksight-template-visual-combochartvisual"></a>
A combo chart\.  
For more information, see [Using combo charts](https://docs.aws.amazon.com/quicksight/latest/user/combo-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [ComboChartVisual](aws-properties-quicksight-template-combochartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomContentVisual`  <a name="cfn-quicksight-template-visual-customcontentvisual"></a>
A visual that contains custom content\.  
For more information, see [Using custom visual content](https://docs.aws.amazon.com/quicksight/latest/user/custom-visual-content.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [CustomContentVisual](aws-properties-quicksight-template-customcontentvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmptyVisual`  <a name="cfn-quicksight-template-visual-emptyvisual"></a>
An empty visual\.  
*Required*: No  
*Type*: [EmptyVisual](aws-properties-quicksight-template-emptyvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilledMapVisual`  <a name="cfn-quicksight-template-visual-filledmapvisual"></a>
A filled map\.  
For more information, see [Creating filled maps](https://docs.aws.amazon.com/quicksight/latest/user/filled-maps.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [FilledMapVisual](aws-properties-quicksight-template-filledmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunnelChartVisual`  <a name="cfn-quicksight-template-visual-funnelchartvisual"></a>
A funnel chart\.  
For more information, see [Using funnel charts](https://docs.aws.amazon.com/quicksight/latest/user/funnel-visual-content.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [FunnelChartVisual](aws-properties-quicksight-template-funnelchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GaugeChartVisual`  <a name="cfn-quicksight-template-visual-gaugechartvisual"></a>
A gauge chart\.  
For more information, see [Using gauge charts](https://docs.aws.amazon.com/quicksight/latest/user/gauge-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [GaugeChartVisual](aws-properties-quicksight-template-gaugechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeospatialMapVisual`  <a name="cfn-quicksight-template-visual-geospatialmapvisual"></a>
A geospatial map or a points on map visual\.  
For more information, see [Creating point maps](https://docs.aws.amazon.com/quicksight/latest/user/point-maps.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [GeospatialMapVisual](aws-properties-quicksight-template-geospatialmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatMapVisual`  <a name="cfn-quicksight-template-visual-heatmapvisual"></a>
A heat map\.  
For more information, see [Using heat maps](https://docs.aws.amazon.com/quicksight/latest/user/heat-map.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [HeatMapVisual](aws-properties-quicksight-template-heatmapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HistogramVisual`  <a name="cfn-quicksight-template-visual-histogramvisual"></a>
A histogram\.  
For more information, see [Using histograms](https://docs.aws.amazon.com/quicksight/latest/user/histogram-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [HistogramVisual](aws-properties-quicksight-template-histogramvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsightVisual`  <a name="cfn-quicksight-template-visual-insightvisual"></a>
An insight visual\.  
For more information, see [Working with insights](https://docs.aws.amazon.com/quicksight/latest/user/computational-insights.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [InsightVisual](aws-properties-quicksight-template-insightvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KPIVisual`  <a name="cfn-quicksight-template-visual-kpivisual"></a>
A key performance indicator \(KPI\)\.  
For more information, see [Using KPIs](https://docs.aws.amazon.com/quicksight/latest/user/kpi.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [KPIVisual](aws-properties-quicksight-template-kpivisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineChartVisual`  <a name="cfn-quicksight-template-visual-linechartvisual"></a>
A line chart\.  
For more information, see [Using line charts](https://docs.aws.amazon.com/quicksight/latest/user/line-charts.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [LineChartVisual](aws-properties-quicksight-template-linechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PieChartVisual`  <a name="cfn-quicksight-template-visual-piechartvisual"></a>
A pie or donut chart\.  
For more information, see [Using pie charts](https://docs.aws.amazon.com/quicksight/latest/user/pie-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [PieChartVisual](aws-properties-quicksight-template-piechartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PivotTableVisual`  <a name="cfn-quicksight-template-visual-pivottablevisual"></a>
A pivot table\.  
For more information, see [Using pivot tables](https://docs.aws.amazon.com/quicksight/latest/user/pivot-table.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [PivotTableVisual](aws-properties-quicksight-template-pivottablevisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RadarChartVisual`  <a name="cfn-quicksight-template-visual-radarchartvisual"></a>
A radar chart visual\.  
For more information, see [Using radar charts](https://docs.aws.amazon.com/quicksight/latest/user/radar-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [RadarChartVisual](aws-properties-quicksight-template-radarchartvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SankeyDiagramVisual`  <a name="cfn-quicksight-template-visual-sankeydiagramvisual"></a>
A sankey diagram\.  
For more information, see [Using Sankey diagrams](https://docs.aws.amazon.com/quicksight/latest/user/sankey-diagram.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [SankeyDiagramVisual](aws-properties-quicksight-template-sankeydiagramvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScatterPlotVisual`  <a name="cfn-quicksight-template-visual-scatterplotvisual"></a>
A scatter plot\.  
For more information, see [Using scatter plots](https://docs.aws.amazon.com/quicksight/latest/user/scatter-plot.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [ScatterPlotVisual](aws-properties-quicksight-template-scatterplotvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableVisual`  <a name="cfn-quicksight-template-visual-tablevisual"></a>
A table visual\.  
For more information, see [Using tables as visuals](https://docs.aws.amazon.com/quicksight/latest/user/tabular.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [TableVisual](aws-properties-quicksight-template-tablevisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreeMapVisual`  <a name="cfn-quicksight-template-visual-treemapvisual"></a>
A tree map\.  
For more information, see [Using tree maps](https://docs.aws.amazon.com/quicksight/latest/user/tree-map.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [TreeMapVisual](aws-properties-quicksight-template-treemapvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaterfallVisual`  <a name="cfn-quicksight-template-visual-waterfallvisual"></a>
A waterfall chart\.  
For more information, see [Using waterfall charts](https://docs.aws.amazon.com/quicksight/latest/user/waterfall-chart.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [WaterfallVisual](aws-properties-quicksight-template-waterfallvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WordCloudVisual`  <a name="cfn-quicksight-template-visual-wordcloudvisual"></a>
A word cloud\.  
For more information, see [Using word clouds](https://docs.aws.amazon.com/quicksight/latest/user/word-cloud.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [WordCloudVisual](aws-properties-quicksight-template-wordcloudvisual.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)