# AWS::QuickSight::Dashboard TableVisual<a name="aws-properties-quicksight-dashboard-tablevisual"></a>

A table visual\.

For more information, see [Using tables as visuals](https://docs.aws.amazon.com/quicksight/latest/user/tabular.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablevisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablevisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-tablevisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-dashboard-tablevisual-chartconfiguration)" : TableConfiguration,
  "[ConditionalFormatting](#cfn-quicksight-dashboard-tablevisual-conditionalformatting)" : TableConditionalFormatting,
  "[Subtitle](#cfn-quicksight-dashboard-tablevisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-tablevisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-tablevisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablevisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-tablevisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-dashboard-tablevisual-chartconfiguration): 
    TableConfiguration
  [ConditionalFormatting](#cfn-quicksight-dashboard-tablevisual-conditionalformatting): 
    TableConditionalFormatting
  [Subtitle](#cfn-quicksight-dashboard-tablevisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-tablevisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-tablevisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-tablevisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-tablevisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-dashboard-tablevisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [TableConfiguration](aws-properties-quicksight-dashboard-tableconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-dashboard-tablevisual-conditionalformatting"></a>
The conditional formatting for a `PivotTableVisual`\.  
*Required*: No  
*Type*: [TableConditionalFormatting](aws-properties-quicksight-dashboard-tableconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-tablevisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-tablevisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-tablevisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)