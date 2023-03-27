# AWS::Kendra::DataSource SalesforceChatterFeedConfiguration<a name="aws-properties-kendra-datasource-salesforcechatterfeedconfiguration"></a>

The configuration information for syncing a Salesforce chatter feed\. The contents of the object comes from the Salesforce FeedItem table\.

## Syntax<a name="aws-properties-kendra-datasource-salesforcechatterfeedconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforcechatterfeedconfiguration-syntax.json"></a>

```
{
  "[DocumentDataFieldName](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-documentdatafieldname)" : String,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-documenttitlefieldname)" : String,
  "[FieldMappings](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ],
  "[IncludeFilterTypes](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-includefiltertypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforcechatterfeedconfiguration-syntax.yaml"></a>

```
  [DocumentDataFieldName](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-documentdatafieldname): String
  [DocumentTitleFieldName](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-documenttitlefieldname): String
  [FieldMappings](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
  [IncludeFilterTypes](#cfn-kendra-datasource-salesforcechatterfeedconfiguration-includefiltertypes): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-salesforcechatterfeedconfiguration-properties"></a>

`DocumentDataFieldName`  <a name="cfn-kendra-datasource-salesforcechatterfeedconfiguration-documentdatafieldname"></a>
The name of the column in the Salesforce FeedItem table that contains the content to index\. Typically this is the `Body` column\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleFieldName`  <a name="cfn-kendra-datasource-salesforcechatterfeedconfiguration-documenttitlefieldname"></a>
The name of the column in the Salesforce FeedItem table that contains the title of the document\. This is typically the `Title` column\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-salesforcechatterfeedconfiguration-fieldmappings"></a>
Maps fields from a Salesforce chatter feed into Amazon Kendra index fields\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeFilterTypes`  <a name="cfn-kendra-datasource-salesforcechatterfeedconfiguration-includefiltertypes"></a>
Filters the documents in the feed based on status of the user\. When you specify `ACTIVE_USERS` only documents from users who have an active account are indexed\. When you specify `STANDARD_USER` only documents for Salesforce standard users are documented\. You can specify both\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)