# AWS::QuickSight::Template HistogramVisual<a name="aws-properties-quicksight-template-histogramvisual"></a>

A histogram\.

For more information, see [Using histograms](https://docs.aws.amazon.com/quicksight/latest/user/histogram-charts.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-template-histogramvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-histogramvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-template-histogramvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-template-histogramvisual-chartconfiguration)" : HistogramConfiguration,
  "[Subtitle](#cfn-quicksight-template-histogramvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-template-histogramvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-template-histogramvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-histogramvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-template-histogramvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-template-histogramvisual-chartconfiguration): 
    HistogramConfiguration
  [Subtitle](#cfn-quicksight-template-histogramvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-template-histogramvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-template-histogramvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-template-histogramvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-template-histogramvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-template-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-template-histogramvisual-chartconfiguration"></a>
The configuration for a `HistogramVisual`\.  
*Required*: No  
*Type*: [HistogramConfiguration](aws-properties-quicksight-template-histogramconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-template-histogramvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-template-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-histogramvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-template-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-template-histogramvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)