# AWS::QuickSight::Template SectionBasedLayoutConfiguration<a name="aws-properties-quicksight-template-sectionbasedlayoutconfiguration"></a>

The configuration for a section\-based layout\.

## Syntax<a name="aws-properties-quicksight-template-sectionbasedlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-sectionbasedlayoutconfiguration-syntax.json"></a>

```
{
  "[BodySections](#cfn-quicksight-template-sectionbasedlayoutconfiguration-bodysections)" : [ BodySectionConfiguration, ... ],
  "[CanvasSizeOptions](#cfn-quicksight-template-sectionbasedlayoutconfiguration-canvassizeoptions)" : SectionBasedLayoutCanvasSizeOptions,
  "[FooterSections](#cfn-quicksight-template-sectionbasedlayoutconfiguration-footersections)" : [ HeaderFooterSectionConfiguration, ... ],
  "[HeaderSections](#cfn-quicksight-template-sectionbasedlayoutconfiguration-headersections)" : [ HeaderFooterSectionConfiguration, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-sectionbasedlayoutconfiguration-syntax.yaml"></a>

```
  [BodySections](#cfn-quicksight-template-sectionbasedlayoutconfiguration-bodysections): 
    - BodySectionConfiguration
  [CanvasSizeOptions](#cfn-quicksight-template-sectionbasedlayoutconfiguration-canvassizeoptions): 
    SectionBasedLayoutCanvasSizeOptions
  [FooterSections](#cfn-quicksight-template-sectionbasedlayoutconfiguration-footersections): 
    - HeaderFooterSectionConfiguration
  [HeaderSections](#cfn-quicksight-template-sectionbasedlayoutconfiguration-headersections): 
    - HeaderFooterSectionConfiguration
```

## Properties<a name="aws-properties-quicksight-template-sectionbasedlayoutconfiguration-properties"></a>

`BodySections`  <a name="cfn-quicksight-template-sectionbasedlayoutconfiguration-bodysections"></a>
A list of body section configurations\.  
*Required*: Yes  
*Type*: List of [BodySectionConfiguration](aws-properties-quicksight-template-bodysectionconfiguration.md)  
*Maximum*: `28`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CanvasSizeOptions`  <a name="cfn-quicksight-template-sectionbasedlayoutconfiguration-canvassizeoptions"></a>
The options for the canvas of a section\-based layout\.  
*Required*: Yes  
*Type*: [SectionBasedLayoutCanvasSizeOptions](aws-properties-quicksight-template-sectionbasedlayoutcanvassizeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FooterSections`  <a name="cfn-quicksight-template-sectionbasedlayoutconfiguration-footersections"></a>
A list of footer section configurations\.  
*Required*: Yes  
*Type*: List of [HeaderFooterSectionConfiguration](aws-properties-quicksight-template-headerfootersectionconfiguration.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderSections`  <a name="cfn-quicksight-template-sectionbasedlayoutconfiguration-headersections"></a>
A list of header section configurations\.  
*Required*: Yes  
*Type*: List of [HeaderFooterSectionConfiguration](aws-properties-quicksight-template-headerfootersectionconfiguration.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)