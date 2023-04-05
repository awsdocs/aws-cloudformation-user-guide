# AWS::QuickSight::Analysis TableVisual<a name="aws-properties-quicksight-analysis-tablevisual"></a>

A table visual\.

For more information, see [Using tables as visuals](https://docs.aws.amazon.com/quicksight/latest/user/tabular.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-analysis-tablevisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tablevisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-analysis-tablevisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-analysis-tablevisual-chartconfiguration)" : TableConfiguration,
  "[ConditionalFormatting](#cfn-quicksight-analysis-tablevisual-conditionalformatting)" : TableConditionalFormatting,
  "[Subtitle](#cfn-quicksight-analysis-tablevisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-analysis-tablevisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-analysis-tablevisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-tablevisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-analysis-tablevisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-analysis-tablevisual-chartconfiguration): 
    TableConfiguration
  [ConditionalFormatting](#cfn-quicksight-analysis-tablevisual-conditionalformatting): 
    TableConditionalFormatting
  [Subtitle](#cfn-quicksight-analysis-tablevisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-analysis-tablevisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-analysis-tablevisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-analysis-tablevisual-properties"></a>

`Actions`  <a name="cfn-quicksight-analysis-tablevisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-analysis-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-analysis-tablevisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [TableConfiguration](aws-properties-quicksight-analysis-tableconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-analysis-tablevisual-conditionalformatting"></a>
The conditional formatting for a `PivotTableVisual`\.  
*Required*: No  
*Type*: [TableConditionalFormatting](aws-properties-quicksight-analysis-tableconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-analysis-tablevisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-analysis-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-tablevisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-analysis-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-analysis-tablevisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)