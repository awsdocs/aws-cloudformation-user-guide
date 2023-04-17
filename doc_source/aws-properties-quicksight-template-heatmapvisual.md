# AWS::QuickSight::Template HeatMapVisual<a name="aws-properties-quicksight-template-heatmapvisual"></a>

A heat map\.

For more information, see [Using heat maps](https://docs.aws.amazon.com/quicksight/latest/user/heat-map.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-template-heatmapvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-heatmapvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-template-heatmapvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-template-heatmapvisual-chartconfiguration)" : HeatMapConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-template-heatmapvisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[Subtitle](#cfn-quicksight-template-heatmapvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-template-heatmapvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-template-heatmapvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-heatmapvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-template-heatmapvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-template-heatmapvisual-chartconfiguration): 
    HeatMapConfiguration
  [ColumnHierarchies](#cfn-quicksight-template-heatmapvisual-columnhierarchies): 
    - ColumnHierarchy
  [Subtitle](#cfn-quicksight-template-heatmapvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-template-heatmapvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-template-heatmapvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-template-heatmapvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-template-heatmapvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-template-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-template-heatmapvisual-chartconfiguration"></a>
The configuration of a heat map\.  
*Required*: No  
*Type*: [HeatMapConfiguration](aws-properties-quicksight-template-heatmapconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-template-heatmapvisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-template-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-template-heatmapvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-template-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-heatmapvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-template-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-template-heatmapvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)