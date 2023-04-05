# AWS::QuickSight::Dashboard FilledMapVisual<a name="aws-properties-quicksight-dashboard-filledmapvisual"></a>

A filled map\.

For more information, see [Creating filled maps](https://docs.aws.amazon.com/quicksight/latest/user/filled-maps.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-filledmapvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filledmapvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-filledmapvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-dashboard-filledmapvisual-chartconfiguration)" : FilledMapConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-dashboard-filledmapvisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[ConditionalFormatting](#cfn-quicksight-dashboard-filledmapvisual-conditionalformatting)" : FilledMapConditionalFormatting,
  "[Subtitle](#cfn-quicksight-dashboard-filledmapvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-filledmapvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-filledmapvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filledmapvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-filledmapvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-dashboard-filledmapvisual-chartconfiguration): 
    FilledMapConfiguration
  [ColumnHierarchies](#cfn-quicksight-dashboard-filledmapvisual-columnhierarchies): 
    - ColumnHierarchy
  [ConditionalFormatting](#cfn-quicksight-dashboard-filledmapvisual-conditionalformatting): 
    FilledMapConditionalFormatting
  [Subtitle](#cfn-quicksight-dashboard-filledmapvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-filledmapvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-filledmapvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-filledmapvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-filledmapvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-dashboard-filledmapvisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [FilledMapConfiguration](aws-properties-quicksight-dashboard-filledmapconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-dashboard-filledmapvisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-dashboard-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-dashboard-filledmapvisual-conditionalformatting"></a>
The conditional formatting of a `FilledMapVisual`\.  
*Required*: No  
*Type*: [FilledMapConditionalFormatting](aws-properties-quicksight-dashboard-filledmapconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-filledmapvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-filledmapvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-filledmapvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)