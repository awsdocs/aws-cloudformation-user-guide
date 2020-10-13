# AWS::Kendra::DataSource SalesforceCustomKnowledgeArticleTypeConfiguration<a name="aws-properties-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration"></a>

Provides configuration information for indexing Salesforce custom articles\.

## Syntax<a name="aws-properties-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-syntax.json"></a>

```
{
  "[DocumentDataFieldName](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-documentdatafieldname)" : String,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-documenttitlefieldname)" : String,
  "[FieldMappings](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-fieldmappings)" : DataSourceToIndexFieldMappingList,
  "[Name](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-name)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-syntax.yaml"></a>

```
  [DocumentDataFieldName](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-documentdatafieldname): String
  [DocumentTitleFieldName](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-documenttitlefieldname): String
  [FieldMappings](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-fieldmappings): 
    DataSourceToIndexFieldMappingList
  [Name](#cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-name): String
```

## Properties<a name="aws-properties-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-properties"></a>

`DocumentDataFieldName`  <a name="cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-documentdatafieldname"></a>
The name of the field in the custom knowledge article that contains the document data to index\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleFieldName`  <a name="cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-documenttitlefieldname"></a>
The name of the field in the custom knowledge article that contains the document title\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-fieldmappings"></a>
One or more objects that map fields in the custom knowledge article to fields in the Amazon Kendra index\.  
*Required*: No  
*Type*: [DataSourceToIndexFieldMappingList](aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kendra-datasource-salesforcecustomknowledgearticletypeconfiguration-name"></a>
The name of the configuration\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)