# AWS::QuickSight::Analysis BodySectionContent<a name="aws-properties-quicksight-analysis-bodysectioncontent"></a>

The configuration of content in a body section\.

## Syntax<a name="aws-properties-quicksight-analysis-bodysectioncontent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-bodysectioncontent-syntax.json"></a>

```
{
  "[Layout](#cfn-quicksight-analysis-bodysectioncontent-layout)" : SectionLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-bodysectioncontent-syntax.yaml"></a>

```
  [Layout](#cfn-quicksight-analysis-bodysectioncontent-layout): 
    SectionLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-bodysectioncontent-properties"></a>

`Layout`  <a name="cfn-quicksight-analysis-bodysectioncontent-layout"></a>
The layout configuration of a body section\.  
*Required*: No  
*Type*: [SectionLayoutConfiguration](aws-properties-quicksight-analysis-sectionlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)