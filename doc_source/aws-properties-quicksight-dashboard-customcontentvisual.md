# AWS::QuickSight::Dashboard CustomContentVisual<a name="aws-properties-quicksight-dashboard-customcontentvisual"></a>

A visual that contains custom content\.

For more information, see [Using custom visual content](https://docs.aws.amazon.com/quicksight/latest/user/custom-visual-content.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-customcontentvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-customcontentvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-dashboard-customcontentvisual-actions)" : [ VisualCustomAction, ... ],
  "[ChartConfiguration](#cfn-quicksight-dashboard-customcontentvisual-chartconfiguration)" : CustomContentConfiguration,
  "[DataSetIdentifier](#cfn-quicksight-dashboard-customcontentvisual-datasetidentifier)" : String,
  "[Subtitle](#cfn-quicksight-dashboard-customcontentvisual-subtitle)" : VisualSubtitleLabelOptions,
  "[Title](#cfn-quicksight-dashboard-customcontentvisual-title)" : VisualTitleLabelOptions,
  "[VisualId](#cfn-quicksight-dashboard-customcontentvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-customcontentvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-dashboard-customcontentvisual-actions): 
    - VisualCustomAction
  [ChartConfiguration](#cfn-quicksight-dashboard-customcontentvisual-chartconfiguration): 
    CustomContentConfiguration
  [DataSetIdentifier](#cfn-quicksight-dashboard-customcontentvisual-datasetidentifier): String
  [Subtitle](#cfn-quicksight-dashboard-customcontentvisual-subtitle): 
    VisualSubtitleLabelOptions
  [Title](#cfn-quicksight-dashboard-customcontentvisual-title): 
    VisualTitleLabelOptions
  [VisualId](#cfn-quicksight-dashboard-customcontentvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-customcontentvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-dashboard-customcontentvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-dashboard-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChartConfiguration`  <a name="cfn-quicksight-dashboard-customcontentvisual-chartconfiguration"></a>
The configuration of a `CustomContentVisual`\.  
*Required*: No  
*Type*: [CustomContentConfiguration](aws-properties-quicksight-dashboard-customcontentconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetIdentifier`  <a name="cfn-quicksight-dashboard-customcontentvisual-datasetidentifier"></a>
The dataset that is used to create the custom content visual\. You can't create a visual without a dataset\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-quicksight-dashboard-customcontentvisual-subtitle"></a>
The subtitle that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualSubtitleLabelOptions](aws-properties-quicksight-dashboard-visualsubtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-customcontentvisual-title"></a>
The title that is displayed on the visual\.  
*Required*: No  
*Type*: [VisualTitleLabelOptions](aws-properties-quicksight-dashboard-visualtitlelabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-dashboard-customcontentvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)