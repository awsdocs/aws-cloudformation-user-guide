# AWS::Kendra::DataSource ServiceNowServiceCatalogConfiguration<a name="aws-properties-kendra-datasource-servicenowservicecatalogconfiguration"></a>

Provides configuration information for crawling service catalog items in the ServiceNow site

## Syntax<a name="aws-properties-kendra-datasource-servicenowservicecatalogconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-servicenowservicecatalogconfiguration-syntax.json"></a>

```
{
  "[CrawlAttachments](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-crawlattachments)" : Boolean,
  "[DocumentDataFieldName](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-documentdatafieldname)" : String,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-documenttitlefieldname)" : String,
  "[ExcludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-excludeattachmentfilepatterns)" : DataSourceInclusionsExclusionsStrings,
  "[FieldMappings](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-fieldmappings)" : DataSourceToIndexFieldMappingList,
  "[IncludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-includeattachmentfilepatterns)" : DataSourceInclusionsExclusionsStrings
}
```

### YAML<a name="aws-properties-kendra-datasource-servicenowservicecatalogconfiguration-syntax.yaml"></a>

```
  [CrawlAttachments](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-crawlattachments): Boolean
  [DocumentDataFieldName](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-documentdatafieldname): String
  [DocumentTitleFieldName](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-documenttitlefieldname): String
  [ExcludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-excludeattachmentfilepatterns): 
    DataSourceInclusionsExclusionsStrings
  [FieldMappings](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-fieldmappings): 
    DataSourceToIndexFieldMappingList
  [IncludeAttachmentFilePatterns](#cfn-kendra-datasource-servicenowservicecatalogconfiguration-includeattachmentfilepatterns): 
    DataSourceInclusionsExclusionsStrings
```

## Properties<a name="aws-properties-kendra-datasource-servicenowservicecatalogconfiguration-properties"></a>

`CrawlAttachments`  <a name="cfn-kendra-datasource-servicenowservicecatalogconfiguration-crawlattachments"></a>
Indicates whether Amazon Kendra should crawl attachments to the service catalog items\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentDataFieldName`  <a name="cfn-kendra-datasource-servicenowservicecatalogconfiguration-documentdatafieldname"></a>
The name of the ServiceNow field that is mapped to the index document contents field in the Amazon Kendra index\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleFieldName`  <a name="cfn-kendra-datasource-servicenowservicecatalogconfiguration-documenttitlefieldname"></a>
The name of the ServiceNow field that is mapped to the index document title field\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeAttachmentFilePatterns`  <a name="cfn-kendra-datasource-servicenowservicecatalogconfiguration-excludeattachmentfilepatterns"></a>
Determines the types of file attachments that are excluded from the index\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-servicenowservicecatalogconfiguration-fieldmappings"></a>
Mapping between ServiceNow fields and Amazon Kendra index fields\. You must create the index field before you map the field\.  
*Required*: No  
*Type*: [DataSourceToIndexFieldMappingList](aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeAttachmentFilePatterns`  <a name="cfn-kendra-datasource-servicenowservicecatalogconfiguration-includeattachmentfilepatterns"></a>
Determines the types of file attachments that are included in the index\.   
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)