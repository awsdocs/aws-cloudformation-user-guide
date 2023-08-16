# AWS::QuickSight::Dashboard InsightVisual<a name="aws-properties-quicksight-dashboard-insightvisual"></a>

An insight visual\.

For more information, see [Working with insights](https://docs.aws.amazon.com/quicksight/latest/user/computational-insights.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-insightvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-insightvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-insightvisual-actions)" : [ VisualCustomAction, ... ],
  "[DataSetIdentifier](#cfn-quicksight-dashboard-insightvisual-datasetidentifier)" : String,
  "[InsightConfiguration](#cfn-quicksight-dashboard-insightvisual-insightconfiguration)" : InsightConfiguration,
  "[Subtitle](#cfn-quicksight-dashboard-insightvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-insightvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-insightvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-insightvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-insightvisual-actions): 
    - VisualCustomAction
  [DataSetIdentifier](#cfn-quicksight-dashboard-insightvisual-datasetidentifier): String
  [InsightConfiguration](#cfn-quicksight-dashboard-insightvisual-insightconfiguration): 
    InsightConfiguration
  [Subtitle](#cfn-quicksight-dashboard-insightvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-insightvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-insightvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-insightvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-insightvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetIdentifier`  <a name="cfn-quicksight-dashboard-insightvisual-datasetidentifier"></a>
The dataset that is used in the insight visual\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsightConfiguration`  <a name="cfn-quicksight-dashboard-insightvisual-insightconfiguration"></a>
The configuration of an insight visual\.  
*Required*: No  
*Type*: [InsightConfiguration](aws-properties-quicksight-dashboard-insightconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-insightvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-insightvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-insightvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)