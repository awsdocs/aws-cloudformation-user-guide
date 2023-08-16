# AWS::QuickSight::Template FilledMapVisual<a name="aws-properties-quicksight-template-filledmapvisual"></a>

A filled map\.

For more information, see [Creating filled maps](https://docs.aws.amazon.com/quicksight/latest/user/filled-maps.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-template-filledmapvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filledmapvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-template-filledmapvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-template-filledmapvisual-chartconfiguration)" : FilledMapConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-template-filledmapvisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[ConditionalFormatting](#cfn-quicksight-template-filledmapvisual-conditionalformatting)" : FilledMapConditionalFormatting,
  "[Subtitle](#cfn-quicksight-template-filledmapvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-template-filledmapvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-template-filledmapvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-filledmapvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-template-filledmapvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-template-filledmapvisual-chartconfiguration): 
    FilledMapConfiguration
  [ColumnHierarchies](#cfn-quicksight-template-filledmapvisual-columnhierarchies): 
    - ColumnHierarchy
  [ConditionalFormatting](#cfn-quicksight-template-filledmapvisual-conditionalformatting): 
    FilledMapConditionalFormatting
  [Subtitle](#cfn-quicksight-template-filledmapvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-template-filledmapvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-template-filledmapvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-template-filledmapvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-template-filledmapvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-template-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-template-filledmapvisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [FilledMapConfiguration](aws-properties-quicksight-template-filledmapconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-template-filledmapvisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-template-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionalFormatting`  <a name="cfn-quicksight-template-filledmapvisual-conditionalformatting"></a>
The conditional formatting of a `FilledMapVisual`\.  
*Required*: No  
*Type*: [FilledMapConditionalFormatting](aws-properties-quicksight-template-filledmapconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-template-filledmapvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-template-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-filledmapvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-template-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-template-filledmapvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)