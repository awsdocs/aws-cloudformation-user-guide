# AWS::QuickSight::Analysis DefaultPaginatedLayoutConfiguration<a name="aws-properties-quicksight-analysis-defaultpaginatedlayoutconfiguration"></a>

The options that determine the default settings for a paginated layout configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-defaultpaginatedlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-defaultpaginatedlayoutconfiguration-syntax.json"></a>

```
{
  "[SectionBased](#cfn-quicksight-analysis-defaultpaginatedlayoutconfiguration-sectionbased)" : DefaultSectionBasedLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-defaultpaginatedlayoutconfiguration-syntax.yaml"></a>

```
  [SectionBased](#cfn-quicksight-analysis-defaultpaginatedlayoutconfiguration-sectionbased): 
    DefaultSectionBasedLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-defaultpaginatedlayoutconfiguration-properties"></a>

`SectionBased`  <a name="cfn-quicksight-analysis-defaultpaginatedlayoutconfiguration-sectionbased"></a>
The options that determine the default settings for a section\-based layout configuration\.  
*Required*: No  
*Type*: [DefaultSectionBasedLayoutConfiguration](aws-properties-quicksight-analysis-defaultsectionbasedlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)