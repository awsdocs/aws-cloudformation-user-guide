# AWS::QuickSight::Analysis GeospatialMapVisual<a name="aws-properties-quicksight-analysis-geospatialmapvisual"></a>

A geospatial map or a points on map visual\.

For more information, see [Creating point maps](https://docs.aws.amazon.com/quicksight/latest/user/point-maps.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-analysis-geospatialmapvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-geospatialmapvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-analysis-geospatialmapvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-analysis-geospatialmapvisual-chartconfiguration)" : GeospatialMapConfiguration,
  "[ColumnHierarchies](#cfn-quicksight-analysis-geospatialmapvisual-columnhierarchies)" : [ ColumnHierarchy, ... ],
  "[Subtitle](#cfn-quicksight-analysis-geospatialmapvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-analysis-geospatialmapvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-analysis-geospatialmapvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-geospatialmapvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-analysis-geospatialmapvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-analysis-geospatialmapvisual-chartconfiguration): 
    GeospatialMapConfiguration
  [ColumnHierarchies](#cfn-quicksight-analysis-geospatialmapvisual-columnhierarchies): 
    - ColumnHierarchy
  [Subtitle](#cfn-quicksight-analysis-geospatialmapvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-analysis-geospatialmapvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-analysis-geospatialmapvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-analysis-geospatialmapvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-analysis-geospatialmapvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-analysis-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-analysis-geospatialmapvisual-chartconfiguration"></a>
The configuration settings of the visual\.  
*Required*: No  
*Type*: [GeospatialMapConfiguration](aws-properties-quicksight-analysis-geospatialmapconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnHierarchies`  <a name="cfn-quicksight-analysis-geospatialmapvisual-columnhierarchies"></a>
The column hierarchy that is used during drill\-downs and drill\-ups\.  
*Required*: No  
*Type*: List of [ColumnHierarchy](aws-properties-quicksight-analysis-columnhierarchy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-analysis-geospatialmapvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-analysis-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-geospatialmapvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-analysis-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-analysis-geospatialmapvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)