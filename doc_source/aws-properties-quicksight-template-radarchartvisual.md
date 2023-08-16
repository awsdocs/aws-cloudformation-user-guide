# AWS::QuickSight::Template RadarChartVisual<a name="aws-properties-quicksight-template-radarchartvisual"></a>

A radar chart visual\.

## Syntax<a name="aws-properties-quicksight-template-radarchartvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-radarchartvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-template-radarchartvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-template-radarchartvisual-chartconfiguration)" : RadarChartConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-template-radarchartvisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[Subtitle](#cfn-quicksight-template-radarchartvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-template-radarchartvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-template-radarchartvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-radarchartvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-template-radarchartvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-template-radarchartvisual-chartconfiguration): 
    RadarChartConfiguration
  [ColumnHierarchies](#cfn-quicksight-template-radarchartvisual-columnhierarchies): 
    - ColumnHierarchy
  [Subtitle](#cfn-quicksight-template-radarchartvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-template-radarchartvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-template-radarchartvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-template-radarchartvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-template-radarchartvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-template-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-template-radarchartvisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [RadarChartConfiguration](aws-properties-quicksight-template-radarchartconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-template-radarchartvisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-template-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-template-radarchartvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-template-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-radarchartvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-template-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-template-radarchartvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)