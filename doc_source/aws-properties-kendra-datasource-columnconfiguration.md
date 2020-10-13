# AWS::Kendra::DataSource ColumnConfiguration<a name="aws-properties-kendra-datasource-columnconfiguration"></a>

Provides information about how Amazon Kendra should use the columns of a database in an index\.

## Syntax<a name="aws-properties-kendra-datasource-columnconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-columnconfiguration-syntax.json"></a>

```
{
  "[ChangeDetectingColumns](#cfn-kendra-datasource-columnconfiguration-changedetectingcolumns)" : ChangeDetectingColumns,
  "[DocumentDataColumnName](#cfn-kendra-datasource-columnconfiguration-documentdatacolumnname)" : String,
  "[DocumentIdColumnName](#cfn-kendra-datasource-columnconfiguration-documentidcolumnname)" : String,
  "[DocumentTitleColumnName](#cfn-kendra-datasource-columnconfiguration-documenttitlecolumnname)" : String,
  "[FieldMappings](#cfn-kendra-datasource-columnconfiguration-fieldmappings)" : DataSourceToIndexFieldMappingList
}
```

### YAML<a name="aws-properties-kendra-datasource-columnconfiguration-syntax.yaml"></a>

```
  [ChangeDetectingColumns](#cfn-kendra-datasource-columnconfiguration-changedetectingcolumns): 
    ChangeDetectingColumns
  [DocumentDataColumnName](#cfn-kendra-datasource-columnconfiguration-documentdatacolumnname): String
  [DocumentIdColumnName](#cfn-kendra-datasource-columnconfiguration-documentidcolumnname): String
  [DocumentTitleColumnName](#cfn-kendra-datasource-columnconfiguration-documenttitlecolumnname): String
  [FieldMappings](#cfn-kendra-datasource-columnconfiguration-fieldmappings): 
    DataSourceToIndexFieldMappingList
```

## Properties<a name="aws-properties-kendra-datasource-columnconfiguration-properties"></a>

`ChangeDetectingColumns`  <a name="cfn-kendra-datasource-columnconfiguration-changedetectingcolumns"></a>
One to five columns that indicate when a document in the database has changed\.  
*Required*: Yes  
*Type*: [ChangeDetectingColumns](aws-properties-kendra-datasource-changedetectingcolumns.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentDataColumnName`  <a name="cfn-kendra-datasource-columnconfiguration-documentdatacolumnname"></a>
The column that contains the contents of the document\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentIdColumnName`  <a name="cfn-kendra-datasource-columnconfiguration-documentidcolumnname"></a>
The column that provides the document's unique identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleColumnName`  <a name="cfn-kendra-datasource-columnconfiguration-documenttitlecolumnname"></a>
The column that contains the title of the document\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-columnconfiguration-fieldmappings"></a>
An array of objects that map database column names to the corresponding fields in an index\. You must first create the fields in the index using the [UpdateIndex](https://docs.aws.amazon.com/kendra/latest/dg/API_UpdateIndex.html) operation\.  
*Required*: No  
*Type*: [DataSourceToIndexFieldMappingList](aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)