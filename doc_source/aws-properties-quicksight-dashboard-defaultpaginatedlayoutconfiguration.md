# AWS::QuickSight::Dashboard DefaultPaginatedLayoutConfiguration<a name="aws-properties-quicksight-dashboard-defaultpaginatedlayoutconfiguration"></a>

The options that determine the default settings for a paginated layout configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-defaultpaginatedlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-defaultpaginatedlayoutconfiguration-syntax.json"></a>

```
{
  "[SectionBased](#cfn-quicksight-dashboard-defaultpaginatedlayoutconfiguration-sectionbased)" : DefaultSectionBasedLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-defaultpaginatedlayoutconfiguration-syntax.yaml"></a>

```
  [SectionBased](#cfn-quicksight-dashboard-defaultpaginatedlayoutconfiguration-sectionbased): 
    DefaultSectionBasedLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-defaultpaginatedlayoutconfiguration-properties"></a>

`SectionBased`  <a name="cfn-quicksight-dashboard-defaultpaginatedlayoutconfiguration-sectionbased"></a>
The options that determine the default settings for a section\-based layout configuration\.  
*Required*: No  
*Type*: [DefaultSectionBasedLayoutConfiguration](aws-properties-quicksight-dashboard-defaultsectionbasedlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)