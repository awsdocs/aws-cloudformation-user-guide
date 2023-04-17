# AWS::QuickSight::Dashboard KPIVisual<a name="aws-properties-quicksight-dashboard-kpivisual"></a>

A key performance indicator \(KPI\)\.

For more information, see [Using KPIs](https://docs.aws.amazon.com/quicksight/latest/user/kpi.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-kpivisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-kpivisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-kpivisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-dashboard-kpivisual-chartconfiguration)" : KPIConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-dashboard-kpivisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[ConditionalFormatting](#cfn-quicksight-dashboard-kpivisual-conditionalformatting)" : KPIConditionalFormatting,
  "[Subtitle](#cfn-quicksight-dashboard-kpivisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-kpivisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-kpivisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-kpivisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-kpivisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-dashboard-kpivisual-chartconfiguration): 
    KPIConfiguration
  [ColumnHierarchies](#cfn-quicksight-dashboard-kpivisual-columnhierarchies): 
    - ColumnHierarchy
  [ConditionalFormatting](#cfn-quicksight-dashboard-kpivisual-conditionalformatting): 
    KPIConditionalFormatting
  [Subtitle](#cfn-quicksight-dashboard-kpivisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-kpivisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-kpivisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-kpivisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-kpivisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-dashboard-kpivisual-chartconfiguration"></a>
The configuration of a KPI visual\.  
*Required*: No  
*Type*: [KPIConfiguration](aws-properties-quicksight-dashboard-kpiconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-dashboard-kpivisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-dashboard-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-dashboard-kpivisual-conditionalformatting"></a>
The conditional formatting of a KPI visual\.  
*Required*: No  
*Type*: [KPIConditionalFormatting](aws-properties-quicksight-dashboard-kpiconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-kpivisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-kpivisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-kpivisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)