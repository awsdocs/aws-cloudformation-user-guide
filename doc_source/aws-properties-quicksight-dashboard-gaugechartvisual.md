# AWS::QuickSight::Dashboard GaugeChartVisual<a name="aws-properties-quicksight-dashboard-gaugechartvisual"></a>

A gauge chart\.

For more information, see [Using gauge charts](https://docs.aws.amazon.com/quicksight/latest/user/gauge-chart.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-gaugechartvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-gaugechartvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-gaugechartvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-dashboard-gaugechartvisual-chartconfiguration)" : GaugeChartConfiguration,
  "[ConditionalFormatting](#cfn-quicksight-dashboard-gaugechartvisual-conditionalformatting)" : GaugeChartConditionalFormatting,
  "[Subtitle](#cfn-quicksight-dashboard-gaugechartvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-gaugechartvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-gaugechartvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-gaugechartvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-gaugechartvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-dashboard-gaugechartvisual-chartconfiguration): 
    GaugeChartConfiguration
  [ConditionalFormatting](#cfn-quicksight-dashboard-gaugechartvisual-conditionalformatting): 
    GaugeChartConditionalFormatting
  [Subtitle](#cfn-quicksight-dashboard-gaugechartvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-gaugechartvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-gaugechartvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-gaugechartvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-gaugechartvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-dashboard-gaugechartvisual-chartconfiguration"></a>
The configuration of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [GaugeChartConfiguration](aws-properties-quicksight-dashboard-gaugechartconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-dashboard-gaugechartvisual-conditionalformatting"></a>
The conditional formatting of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [GaugeChartConditionalFormatting](aws-properties-quicksight-dashboard-gaugechartconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-gaugechartvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-gaugechartvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-gaugechartvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)