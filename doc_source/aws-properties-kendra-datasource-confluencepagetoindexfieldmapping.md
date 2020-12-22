# AWS::Kendra::DataSource ConfluencePageToIndexFieldMapping<a name="aws-properties-kendra-datasource-confluencepagetoindexfieldmapping"></a>

Defines the mapping between a field in the Confluence data source to a Amazon Kendra index field\.

You must first create the index field using the API\_UpdateIndex operation\. 

## Syntax<a name="aws-properties-kendra-datasource-confluencepagetoindexfieldmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluencepagetoindexfieldmapping-syntax.json"></a>

```
{
  "[DataSourceFieldName](#cfn-kendra-datasource-confluencepagetoindexfieldmapping-datasourcefieldname)" : String,
  "[DateFieldFormat](#cfn-kendra-datasource-confluencepagetoindexfieldmapping-datefieldformat)" : String,
  "[IndexFieldName](#cfn-kendra-datasource-confluencepagetoindexfieldmapping-indexfieldname)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-confluencepagetoindexfieldmapping-syntax.yaml"></a>

```
  [DataSourceFieldName](#cfn-kendra-datasource-confluencepagetoindexfieldmapping-datasourcefieldname): String
  [DateFieldFormat](#cfn-kendra-datasource-confluencepagetoindexfieldmapping-datefieldformat): String
  [IndexFieldName](#cfn-kendra-datasource-confluencepagetoindexfieldmapping-indexfieldname): String
```

## Properties<a name="aws-properties-kendra-datasource-confluencepagetoindexfieldmapping-properties"></a>

`DataSourceFieldName`  <a name="cfn-kendra-datasource-confluencepagetoindexfieldmapping-datasourcefieldname"></a>
The name of the field in the data source\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `AUTHOR | CONTENT_STATUS | CREATED_DATE | DISPLAY_URL | ITEM_TYPE | LABELS | MODIFIED_DATE | PARENT_ID | SPACE_KEY | SPACE_NAME | URL | VERSION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateFieldFormat`  <a name="cfn-kendra-datasource-confluencepagetoindexfieldmapping-datefieldformat"></a>
The format for date fields in the data source\. If the field specified in `DataSourceFieldName` is a date field you must specify the date format\. If the field is not a date field, an exception is thrown\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `40`  
*Pattern*: `^(?!\s).*(?<!\s)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexFieldName`  <a name="cfn-kendra-datasource-confluencepagetoindexfieldmapping-indexfieldname"></a>
The name of the index field to map to the Confluence data source field\. The index field type must match the Confluence field type\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `30`  
*Pattern*: `^\P{C}*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)