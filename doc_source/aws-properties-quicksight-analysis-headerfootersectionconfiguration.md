# AWS::QuickSight::Analysis HeaderFooterSectionConfiguration<a name="aws-properties-quicksight-analysis-headerfootersectionconfiguration"></a>

The configuration of a header or footer section\.

## Syntax<a name="aws-properties-quicksight-analysis-headerfootersectionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-headerfootersectionconfiguration-syntax.json"></a>

```
{
  "[Layout](#cfn-quicksight-analysis-headerfootersectionconfiguration-layout)" : SectionLayoutConfiguration,
  "[SectionId](#cfn-quicksight-analysis-headerfootersectionconfiguration-sectionid)" : String,
  "[Style](#cfn-quicksight-analysis-headerfootersectionconfiguration-style)" : SectionStyle
}
```

### YAML<a name="aws-properties-quicksight-analysis-headerfootersectionconfiguration-syntax.yaml"></a>

```
  [Layout](#cfn-quicksight-analysis-headerfootersectionconfiguration-layout): 
    SectionLayoutConfiguration
  [SectionId](#cfn-quicksight-analysis-headerfootersectionconfiguration-sectionid): String
  [Style](#cfn-quicksight-analysis-headerfootersectionconfiguration-style): 
    SectionStyle
```

## Properties<a name="aws-properties-quicksight-analysis-headerfootersectionconfiguration-properties"></a>

`Layout`  <a name="cfn-quicksight-analysis-headerfootersectionconfiguration-layout"></a>
The layout configuration of the header or footer section\.  
*Required*: Yes  
*Type*: [SectionLayoutConfiguration](aws-properties-quicksight-analysis-sectionlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SectionId`  <a name="cfn-quicksight-analysis-headerfootersectionconfiguration-sectionid"></a>
The unique identifier of the header or footer section\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Style`  <a name="cfn-quicksight-analysis-headerfootersectionconfiguration-style"></a>
The style options of a header or footer section\.  
*Required*: No  
*Type*: [SectionStyle](aws-properties-quicksight-analysis-sectionstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)