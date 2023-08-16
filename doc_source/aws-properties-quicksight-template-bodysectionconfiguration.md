# AWS::QuickSight::Template BodySectionConfiguration<a name="aws-properties-quicksight-template-bodysectionconfiguration"></a>

The configuration of a body section\.

## Syntax<a name="aws-properties-quicksight-template-bodysectionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-bodysectionconfiguration-syntax.json"></a>

```
{
  "[Content](#cfn-quicksight-template-bodysectionconfiguration-content)" : BodySectionContent,
  "[PageBreakConfiguration](#cfn-quicksight-template-bodysectionconfiguration-pagebreakconfiguration)" : SectionPageBreakConfiguration,
  "[SectionId](#cfn-quicksight-template-bodysectionconfiguration-sectionid)" : String,
  "[Style](#cfn-quicksight-template-bodysectionconfiguration-style)" : SectionStyle
}
```

### YAML<a name="aws-properties-quicksight-template-bodysectionconfiguration-syntax.yaml"></a>

```
  [Content](#cfn-quicksight-template-bodysectionconfiguration-content): 
    BodySectionContent
  [PageBreakConfiguration](#cfn-quicksight-template-bodysectionconfiguration-pagebreakconfiguration): 
    SectionPageBreakConfiguration
  [SectionId](#cfn-quicksight-template-bodysectionconfiguration-sectionid): String
  [Style](#cfn-quicksight-template-bodysectionconfiguration-style): 
    SectionStyle
```

## Properties<a name="aws-properties-quicksight-template-bodysectionconfiguration-properties"></a>

`Content`  <a name="cfn-quicksight-template-bodysectionconfiguration-content"></a>
The configuration of content in a body section\.  
*Required*: Yes  
*Type*: [BodySectionContent](aws-properties-quicksight-template-bodysectioncontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PageBreakConfiguration`  <a name="cfn-quicksight-template-bodysectionconfiguration-pagebreakconfiguration"></a>
The configuration of a page break for a section\.  
*Required*: No  
*Type*: [SectionPageBreakConfiguration](aws-properties-quicksight-template-sectionpagebreakconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SectionId`  <a name="cfn-quicksight-template-bodysectionconfiguration-sectionid"></a>
The unique identifier of a body section\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Style`  <a name="cfn-quicksight-template-bodysectionconfiguration-style"></a>
The style options of a body section\.  
*Required*: No  
*Type*: [SectionStyle](aws-properties-quicksight-template-sectionstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)