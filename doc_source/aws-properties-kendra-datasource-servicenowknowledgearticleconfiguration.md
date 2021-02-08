# AWS::Kendra::DataSource ServiceNowKnowledgeArticleConfiguration<a name="aws-properties-kendra-datasource-servicenowknowledgearticleconfiguration"></a>

Provides configuration information for crawling knowledge articles in the ServiceNow site\.

## Syntax<a name="aws-properties-kendra-datasource-servicenowknowledgearticleconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-servicenowknowledgearticleconfiguration-syntax.json"></a>

```
{
  "[CrawlAttachments](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-crawlattachments)" : Boolean,
  "[DocumentDataFieldName](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-documentdatafieldname)" : String,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-documenttitlefieldname)" : String,
  "[ExcludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-excludeattachmentfilepatterns)" : DataSourceInclusionsExclusionsStrings,
  "[FieldMappings](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-fieldmappings)" : DataSourceToIndexFieldMappingList,
  "[IncludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-includeattachmentfilepatterns)" : DataSourceInclusionsExclusionsStrings
}
```

### YAML<a name="aws-properties-kendra-datasource-servicenowknowledgearticleconfiguration-syntax.yaml"></a>

```
  [CrawlAttachments](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-crawlattachments): Boolean
  [DocumentDataFieldName](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-documentdatafieldname): String
  [DocumentTitleFieldName](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-documenttitlefieldname): String
  [ExcludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-excludeattachmentfilepatterns): 
    DataSourceInclusionsExclusionsStrings
  [FieldMappings](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-fieldmappings): 
    DataSourceToIndexFieldMappingList
  [IncludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowknowledgearticleconfiguration-includeattachmentfilepatterns): 
    DataSourceInclusionsExclusionsStrings
```

## Properties<a name="aws-properties-kendra-datasource-servicenowknowledgearticleconfiguration-properties"></a>

`CrawlAttachments`  <a name="cfn-kendra-datasource-servicenowknowledgearticleconfiguration-crawlattachments"></a>
Indicates whether Amazon Kendra should index attachments to knowledge articles\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentDataFieldName`  <a name="cfn-kendra-datasource-servicenowknowledgearticleconfiguration-documentdatafieldname"></a>
The name of the ServiceNow field that is mapped to the index document contents field in the Amazon Kendra index\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleFieldName`  <a name="cfn-kendra-datasource-servicenowknowledgearticleconfiguration-documenttitlefieldname"></a>
The name of the ServiceNow field that is mapped to the index document title field\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeAttachmentFilePatterns`  <a name="cfn-kendra-datasource-servicenowknowledgearticleconfiguration-excludeattachmentfilepatterns"></a>
List of regular expressions applied to knowledge articles\. Items that don't match the inclusion pattern are not indexed\. The regex is applied to the field specified in the `PatternTargetField`   
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-servicenowknowledgearticleconfiguration-fieldmappings"></a>
Mapping between ServiceNow fields and Amazon Kendra index fields\. You must create the index field before you map the field\.  
*Required*: No  
*Type*: [DataSourceToIndexFieldMappingList](aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeAttachmentFilePatterns`  <a name="cfn-kendra-datasource-servicenowknowledgearticleconfiguration-includeattachmentfilepatterns"></a>
List of regular expressions applied to knowledge articles\. Items that don't match the inclusion pattern are not indexed\. The regex is applied to the field specified in the `PatternTargetField`\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)