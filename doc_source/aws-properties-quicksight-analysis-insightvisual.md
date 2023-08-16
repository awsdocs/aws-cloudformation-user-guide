# AWS::QuickSight::Analysis InsightVisual<a name="aws-properties-quicksight-analysis-insightvisual"></a>

An insight visual\.

For more information, see [Working with insights](https://docs.aws.amazon.com/quicksight/latest/user/computational-insights.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-analysis-insightvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-insightvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-analysis-insightvisual-actions)" : [ VisualCustomAction, ... ],
  "[DataSetIdentifier](#cfn-quicksight-analysis-insightvisual-datasetidentifier)" : String,
  "[InsightConfiguration](#cfn-quicksight-analysis-insightvisual-insightconfiguration)" : InsightConfiguration,
  "[Subtitle](#cfn-quicksight-analysis-insightvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-analysis-insightvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-analysis-insightvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-insightvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-analysis-insightvisual-actions): 
    - VisualCustomAction
  [DataSetIdentifier](#cfn-quicksight-analysis-insightvisual-datasetidentifier): String
  [InsightConfiguration](#cfn-quicksight-analysis-insightvisual-insightconfiguration): 
    InsightConfiguration
  [Subtitle](#cfn-quicksight-analysis-insightvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-analysis-insightvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-analysis-insightvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-analysis-insightvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-analysis-insightvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-analysis-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetIdentifier`  <a name="cfn-quicksight-analysis-insightvisual-datasetidentifier"></a>
The dataset that is used in the insight visual\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsightConfiguration`  <a name="cfn-quicksight-analysis-insightvisual-insightconfiguration"></a>
The configuration of an insight visual\.  
*Required*: No  
*Type*: [InsightConfiguration](aws-properties-quicksight-analysis-insightconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-analysis-insightvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-analysis-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-insightvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-analysis-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-analysis-insightvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)