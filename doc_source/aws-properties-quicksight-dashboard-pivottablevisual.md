# AWS::QuickSight::Dashboard PivotTableVisual<a name="aws-properties-quicksight-dashboard-pivottablevisual"></a>

A pivot table\.

For more information, see [Using pivot tables](https://docs.aws.amazon.com/quicksight/latest/user/pivot-table.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottablevisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottablevisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-pivottablevisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-dashboard-pivottablevisual-chartconfiguration)" : PivotTableConfiguration,
  "[ConditionalFormatting](#cfn-quicksight-dashboard-pivottablevisual-conditionalformatting)" : PivotTableConditionalFormatting,
  "[Subtitle](#cfn-quicksight-dashboard-pivottablevisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-pivottablevisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-pivottablevisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottablevisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-pivottablevisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-dashboard-pivottablevisual-chartconfiguration): 
    PivotTableConfiguration
  [ConditionalFormatting](#cfn-quicksight-dashboard-pivottablevisual-conditionalformatting): 
    PivotTableConditionalFormatting
  [Subtitle](#cfn-quicksight-dashboard-pivottablevisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-pivottablevisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-pivottablevisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottablevisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-pivottablevisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-dashboard-pivottablevisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [PivotTableConfiguration](aws-properties-quicksight-dashboard-pivottableconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-dashboard-pivottablevisual-conditionalformatting"></a>
The conditional formatting for a `PivotTableVisual`\.  
*Required*: No  
*Type*: [PivotTableConditionalFormatting](aws-properties-quicksight-dashboard-pivottableconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-pivottablevisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-pivottablevisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-pivottablevisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)