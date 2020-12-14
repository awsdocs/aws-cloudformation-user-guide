# AWS::Kendra::DataSource SalesforceStandardKnowledgeArticleTypeConfiguration<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration"></a>

Provides configuration information for standard Salesforce knowledge articles\.

## Syntax<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-syntax.json"></a>

```
{
  "[DocumentDataFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documentdatafieldname)" : String,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documenttitlefieldname)" : String,
  "[FieldMappings](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-fieldmappings)" : DataSourceToIndexFieldMappingList
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-syntax.yaml"></a>

```
  [DocumentDataFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documentdatafieldname): String
  [DocumentTitleFieldName](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-documenttitlefieldname): String
  [FieldMappings](#cfn-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration-fieldmappings): 
    DataSourceToIndexFieldMappingList
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
One or more objects that map fields in the knowledge article to Amazon Kendra index fields\. The index field must exist before you can map a Salesforce field to it\.  
*Required*: No  
*Type*: [DataSourceToIndexFieldMappingList](aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)