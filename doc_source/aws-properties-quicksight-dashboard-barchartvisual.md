# AWS::QuickSight::Dashboard BarChartVisual<a name="aws-properties-quicksight-dashboard-barchartvisual"></a>

A bar chart\.

The `BarChartVisual` structure describes a visual that is a member of the bar chart family\. The following charts can be described using this structure:
+ Horizontal bar chart
+ Vertical bar chart
+ Horizontal stacked bar chart
+ Vertical stacked bar chart
+ Horizontal stacked 100% bar chart
+ Vertical stacked 100% bar chart

For more information, see [Using bar charts](https://docs.aws.amazon.com/quicksight/latest/user/bar-charts.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-barchartvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-barchartvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-barchartvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-dashboard-barchartvisual-chartconfiguration)" : BarChartConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-dashboard-barchartvisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[Subtitle](#cfn-quicksight-dashboard-barchartvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-barchartvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-barchartvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-barchartvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-barchartvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-dashboard-barchartvisual-chartconfiguration): 
    BarChartConfiguration
  [ColumnHierarchies](#cfn-quicksight-dashboard-barchartvisual-columnhierarchies): 
    - ColumnHierarchy
  [Subtitle](#cfn-quicksight-dashboard-barchartvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-barchartvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-barchartvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-barchartvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-barchartvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-dashboard-barchartvisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [BarChartConfiguration](aws-properties-quicksight-dashboard-barchartconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-dashboard-barchartvisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-dashboard-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-barchartvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-barchartvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-barchartvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)