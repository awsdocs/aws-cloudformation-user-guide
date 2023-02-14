# AWS::Kendra::DataSource SalesforceStandardKnowledgeArticleTypeConfiguration<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration"></a>

Provides the configuration information for standard Salesforce knowledge articles\.

## Syntax<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-syntax.json"></a>

```
{
  "[DocumentDataFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documentdatafieldname)" : String,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documenttitlefieldname)" : String,
  "[FieldMappings](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-syntax.yaml"></a>

```
  [DocumentDataFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documentdatafieldname): String
  [DocumentTitleFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documenttitlefieldname): String
  [FieldMappings](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
```

## Properties<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-properties"></a>

`DocumentDataFieldName`  <a name="cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documentdatafieldname"></a>
The name of the field that contains the document data to index\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleFieldName`  <a name="cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documenttitlefieldname"></a>
The name of the field that contains the document title\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-fieldmappings"></a>
Maps attributes or field names of the knowledge article to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to Salesforce fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The Salesforce data source field names must exist in your Salesforce custom metadata\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)