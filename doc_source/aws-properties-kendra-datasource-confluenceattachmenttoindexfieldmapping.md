# AWS::Kendra::DataSource ConfluenceAttachmentToIndexFieldMapping<a name="aws-properties-kendra-datasource-confluenceattachmenttoindexfieldmapping"></a>

Defines the mapping between a field in the Confluence data source to a Amazon Kendra index field\.

You must first create the index field using the API\_UpdateIndex operation\. 

## Syntax<a name="aws-properties-kendra-datasource-confluenceattachmenttoindexfieldmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluenceattachmenttoindexfieldmapping-syntax.json"></a>

```
{
  "[DataSourceFieldName](#cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-datasourcefieldname)" : String,
  "[DateFieldFormat](#cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-datefieldformat)" : String,
  "[IndexFieldName](#cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-indexfieldname)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-confluenceattachmenttoindexfieldmapping-syntax.yaml"></a>

```
  [DataSourceFieldName](#cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-datasourcefieldname): String
  [DateFieldFormat](#cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-datefieldformat): String
  [IndexFieldName](#cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-indexfieldname): String
```

## Properties<a name="aws-properties-kendra-datasource-confluenceattachmenttoindexfieldmapping-properties"></a>

`DataSourceFieldName`  <a name="cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-datasourcefieldname"></a>
The name of the field in the data source\.   
You must first create the index field using the API\_UpdateIndex operation\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `AUTHOR | CONTENT_TYPE | CREATED_DATE | DISPLAY_URL | FILE_SIZE | ITEM_TYPE | PARENT_ID | SPACE_KEY | SPACE_NAME | URL | VERSION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateFieldFormat`  <a name="cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-datefieldformat"></a>
The format for date fields in the data source\. If the field specified in `DataSourceFieldName` is a date field you must specify the date format\. If the field is not a date field, an exception is thrown\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `40`  
*Pattern*: `^(?!\s).*(?<!\s)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexFieldName`  <a name="cfn-kendra-datasource-confluenceattachmenttoindexfieldmapping-indexfieldname"></a>
The name of the index field to map to the Confluence data source field\. The index field type must match the Confluence field type\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `30`  
*Pattern*: `^\P{C}*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)