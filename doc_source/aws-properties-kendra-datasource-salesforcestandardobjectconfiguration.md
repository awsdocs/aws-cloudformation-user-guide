# AWS::Kendra::DataSource SalesforceStandardObjectConfiguration<a name="aws-properties-kendra-datasource-salesforcestandardobjectconfiguration"></a>

Specifies configuration information for indexing a single standard object\.

## Syntax<a name="aws-properties-kendra-datasource-salesforcestandardobjectconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforcestandardobjectconfiguration-syntax.json"></a>

```
{
  "[DocumentDataFieldName](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-documentdatafieldname)" : String,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-documenttitlefieldname)" : String,
  "[FieldMappings](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ],
  "[Name](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-name)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforcestandardobjectconfiguration-syntax.yaml"></a>

```
  [DocumentDataFieldName](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-documentdatafieldname): String
  [DocumentTitleFieldName](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-documenttitlefieldname): String
  [FieldMappings](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
  [Name](#cfn-kendra-datasource-salesforcestandardobjectconfiguration-name): String
```

## Properties<a name="aws-properties-kendra-datasource-salesforcestandardobjectconfiguration-properties"></a>

`DocumentDataFieldName`  <a name="cfn-kendra-datasource-salesforcestandardobjectconfiguration-documentdatafieldname"></a>
The name of the field in the standard object table that contains the document contents\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleFieldName`  <a name="cfn-kendra-datasource-salesforcestandardobjectconfiguration-documenttitlefieldname"></a>
The name of the field in the standard object table that contains the document title\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-salesforcestandardobjectconfiguration-fieldmappings"></a>
Maps attributes or field names of the standard object to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to Salesforce fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The Salesforce data source field names must exist in your Salesforce custom metadata\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kendra-datasource-salesforcestandardobjectconfiguration-name"></a>
The name of the standard object\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ACCOUNT | CAMPAIGN | CASE | CONTACT | CONTRACT | DOCUMENT | GROUP | IDEA | LEAD | OPPORTUNITY | PARTNER | PRICEBOOK | PRODUCT | PROFILE | SOLUTION | TASK | USER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)