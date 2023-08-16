# AWS::QuickSight::Analysis KPIVisual<a name="aws-properties-quicksight-analysis-kpivisual"></a>

A key performance indicator \(KPI\)\.

For more information, see [Using KPIs](https://docs.aws.amazon.com/quicksight/latest/user/kpi.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-analysis-kpivisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-kpivisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-analysis-kpivisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-analysis-kpivisual-chartconfiguration)" : KPIConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-analysis-kpivisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[ConditionalFormatting](#cfn-quicksight-analysis-kpivisual-conditionalformatting)" : KPIConditionalFormatting,
  "[Subtitle](#cfn-quicksight-analysis-kpivisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-analysis-kpivisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-analysis-kpivisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-kpivisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-analysis-kpivisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-analysis-kpivisual-chartconfiguration): 
    KPIConfiguration
  [ColumnHierarchies](#cfn-quicksight-analysis-kpivisual-columnhierarchies): 
    - ColumnHierarchy
  [ConditionalFormatting](#cfn-quicksight-analysis-kpivisual-conditionalformatting): 
    KPIConditionalFormatting
  [Subtitle](#cfn-quicksight-analysis-kpivisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-analysis-kpivisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-analysis-kpivisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-analysis-kpivisual-properties"></a>

`Actions`  <a name="cfn-quicksight-analysis-kpivisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-analysis-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-analysis-kpivisual-chartconfiguration"></a>
The configuration of a KPI visual\.  
*Required*: No  
*Type*: [KPIConfiguration](aws-properties-quicksight-analysis-kpiconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-analysis-kpivisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-analysis-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-analysis-kpivisual-conditionalformatting"></a>
The conditional formatting of a KPI visual\.  
*Required*: No  
*Type*: [KPIConditionalFormatting](aws-properties-quicksight-analysis-kpiconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-analysis-kpivisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-analysis-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-kpivisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-analysis-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-analysis-kpivisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)