# AWS::QuickSight::Analysis SectionBasedLayoutConfiguration<a name="aws-properties-quicksight-analysis-sectionbasedlayoutconfiguration"></a>

The configuration for a section\-based layout\.

## Syntax<a name="aws-properties-quicksight-analysis-sectionbasedlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sectionbasedlayoutconfiguration-syntax.json"></a>

```
{
  "[BodySections](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-bodysections)" : [ BodySectionConfiguration, ... ],
  "[CanvasSizeOptions](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-canvassizeoptions)" : SectionBasedLayoutCanvasSizeOptions,
  "[FooterSections](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-footersections)" : [ HeaderFooterSectionConfiguration, ... ],
  "[HeaderSections](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-headersections)" : [ HeaderFooterSectionConfiguration, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-sectionbasedlayoutconfiguration-syntax.yaml"></a>

```
  [BodySections](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-bodysections): 
    - BodySectionConfiguration
  [CanvasSizeOptions](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-canvassizeoptions): 
    SectionBasedLayoutCanvasSizeOptions
  [FooterSections](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-footersections): 
    - HeaderFooterSectionConfiguration
  [HeaderSections](#cfn-quicksight-analysis-sectionbasedlayoutconfiguration-headersections): 
    - HeaderFooterSectionConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-sectionbasedlayoutconfiguration-properties"></a>

`BodySections`  <a name="cfn-quicksight-analysis-sectionbasedlayoutconfiguration-bodysections"></a>
A list of body section configurations\.  
*Required*: Yes  
*Type*: List of [BodySectionConfiguration](aws-properties-quicksight-analysis-bodysectionconfiguration.md)  
*Maximum*: `28`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CanvasSizeOptions`  <a name="cfn-quicksight-analysis-sectionbasedlayoutconfiguration-canvassizeoptions"></a>
The options for the canvas of a section\-based layout\.  
*Required*: Yes  
*Type*: [SectionBasedLayoutCanvasSizeOptions](aws-properties-quicksight-analysis-sectionbasedlayoutcanvassizeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FooterSections`  <a name="cfn-quicksight-analysis-sectionbasedlayoutconfiguration-footersections"></a>
A list of footer section configurations\.  
*Required*: Yes  
*Type*: List of [HeaderFooterSectionConfiguration](aws-properties-quicksight-analysis-headerfootersectionconfiguration.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderSections`  <a name="cfn-quicksight-analysis-sectionbasedlayoutconfiguration-headersections"></a>
A list of header section configurations\.  
*Required*: Yes  
*Type*: List of [HeaderFooterSectionConfiguration](aws-properties-quicksight-analysis-headerfootersectionconfiguration.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)