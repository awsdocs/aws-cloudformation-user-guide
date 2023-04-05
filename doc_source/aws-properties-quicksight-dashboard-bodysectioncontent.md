# AWS::QuickSight::Dashboard BodySectionContent<a name="aws-properties-quicksight-dashboard-bodysectioncontent"></a>

The configuration of content in a body section\.

## Syntax<a name="aws-properties-quicksight-dashboard-bodysectioncontent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-bodysectioncontent-syntax.json"></a>

```
{
  "[Layout](#cfn-quicksight-dashboard-bodysectioncontent-layout)" : SectionLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-bodysectioncontent-syntax.yaml"></a>

```
  [Layout](#cfn-quicksight-dashboard-bodysectioncontent-layout): 
    SectionLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-bodysectioncontent-properties"></a>

`Layout`  <a name="cfn-quicksight-dashboard-bodysectioncontent-layout"></a>
The layout configuration of a body section\.  
*Required*: No  
*Type*: [SectionLayoutConfiguration](aws-properties-quicksight-dashboard-sectionlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)