# AWS::QuickSight::Analysis SankeyDiagramVisual<a name="aws-properties-quicksight-analysis-sankeydiagramvisual"></a>

A sankey diagram\.

For more information, see [Using Sankey diagrams](https://docs.aws.amazon.com/quicksight/latest/user/sankey-diagram.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-analysis-sankeydiagramvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sankeydiagramvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-analysis-sankeydiagramvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-analysis-sankeydiagramvisual-chartconfiguration)" : SankeyDiagramChartConfiguration,
  "[Subtitle](#cfn-quicksight-analysis-sankeydiagramvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-analysis-sankeydiagramvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-analysis-sankeydiagramvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-sankeydiagramvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-analysis-sankeydiagramvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-analysis-sankeydiagramvisual-chartconfiguration): 
    SankeyDiagramChartConfiguration
  [Subtitle](#cfn-quicksight-analysis-sankeydiagramvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-analysis-sankeydiagramvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-analysis-sankeydiagramvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-analysis-sankeydiagramvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-analysis-sankeydiagramvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-analysis-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-analysis-sankeydiagramvisual-chartconfiguration"></a>
The configuration of a sankey diagram\.  
*Required*: No  
*Type*: [SankeyDiagramChartConfiguration](aws-properties-quicksight-analysis-sankeydiagramchartconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-analysis-sankeydiagramvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-analysis-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-sankeydiagramvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-analysis-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-analysis-sankeydiagramvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)