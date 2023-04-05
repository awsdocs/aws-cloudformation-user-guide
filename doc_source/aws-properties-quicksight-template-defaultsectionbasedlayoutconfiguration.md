# AWS::QuickSight::Template DefaultSectionBasedLayoutConfiguration<a name="aws-properties-quicksight-template-defaultsectionbasedlayoutconfiguration"></a>

The options that determine the default settings for a section\-based layout configuration\.

## Syntax<a name="aws-properties-quicksight-template-defaultsectionbasedlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-defaultsectionbasedlayoutconfiguration-syntax.json"></a>

```
{
  "[CanvasSizeOptions](#cfn-quicksight-template-defaultsectionbasedlayoutconfiguration-canvassizeoptions)" : SectionBasedLayoutCanvasSizeOptions
}
```

### YAML<a name="aws-properties-quicksight-template-defaultsectionbasedlayoutconfiguration-syntax.yaml"></a>

```
  [CanvasSizeOptions](#cfn-quicksight-template-defaultsectionbasedlayoutconfiguration-canvassizeoptions): 
    SectionBasedLayoutCanvasSizeOptions
```

## Properties<a name="aws-properties-quicksight-template-defaultsectionbasedlayoutconfiguration-properties"></a>

`CanvasSizeOptions`  <a name="cfn-quicksight-template-defaultsectionbasedlayoutconfiguration-canvassizeoptions"></a>
Determines the screen canvas size options for a section\-based layout\.  
*Required*: Yes  
*Type*: [SectionBasedLayoutCanvasSizeOptions](aws-properties-quicksight-template-sectionbasedlayoutcanvassizeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)