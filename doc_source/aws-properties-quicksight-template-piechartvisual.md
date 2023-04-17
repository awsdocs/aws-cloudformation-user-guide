# AWS::QuickSight::Template PieChartVisual<a name="aws-properties-quicksight-template-piechartvisual"></a>

A pie or donut chart\.

The `PieChartVisual` structure describes a visual that is a member of the pie chart family\.

The following charts can be described by using this structure:
+ Pie charts
+ Donut charts

For more information, see [Using pie charts](https://docs.aws.amazon.com/quicksight/latest/user/pie-chart.html) in the *Amazon QuickSight User Guide*\.

For more information, see [Using donut charts](https://docs.aws.amazon.com/quicksight/latest/user/donut-chart.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-template-piechartvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-piechartvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-template-piechartvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-template-piechartvisual-chartconfiguration)" : PieChartConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-template-piechartvisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[Subtitle](#cfn-quicksight-template-piechartvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-template-piechartvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-template-piechartvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-piechartvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-template-piechartvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-template-piechartvisual-chartconfiguration): 
    PieChartConfiguration
  [ColumnHierarchies](#cfn-quicksight-template-piechartvisual-columnhierarchies): 
    - ColumnHierarchy
  [Subtitle](#cfn-quicksight-template-piechartvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-template-piechartvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-template-piechartvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-template-piechartvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-template-piechartvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-template-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-template-piechartvisual-chartconfiguration"></a>
The configuration of a pie chart\.  
*Required*: No  
*Type*: [PieChartConfiguration](aws-properties-quicksight-template-piechartconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-template-piechartvisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-template-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-template-piechartvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-template-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-piechartvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-template-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-template-piechartvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)