# AWS Glue Table TableInput<a name="aws-properties-glue-table-tableinput"></a>

<a name="aws-properties-glue-table-tableinput-description"></a>The `TableInput` property type specifies the metadata that's used to create or update an AWS Glue table\.

<a name="aws-properties-glue-table-tableinput-inheritance"></a> `TableInput` is a property of the [AWS::Glue::Table](aws-resource-glue-table.md) resource\.

## Syntax<a name="aws-properties-glue-table-tableinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-tableinput-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-owner)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-vieworiginaltext)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-description)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-tabletype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-parameters)" : JSON object,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-viewexpandedtext)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-storagedescriptor)" : StorageDescriptor,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-partitionkeys)" : [ Column, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-retention)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-name)" : String
}
```

### YAML<a name="aws-properties-glue-table-tableinput-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-owner): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-vieworiginaltext): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-description): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-tabletype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-parameters): JSON object
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-viewexpandedtext): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-storagedescriptor): 
  StorageDescriptor
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-partitionkeys): 
  - Column
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-retention): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput-name): String
```

## Properties<a name="aws-properties-glue-table-tableinput-properties"></a>

For more information, see [TableInput Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-TableInput) in the *AWS Glue Developer Guide*\.

`Owner`  
The owner of the table\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ViewOriginalText`  
The original text of the view, if the table is a view\. Otherwise, it's `null`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Description`  
The description of the table\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`TableType`  
The type of the table, such as `EXTERNAL_TABLE` or `VIRTUAL_VIEW`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Parameters`  
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the properties that are associated with the table\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`ViewExpandedText`  
The expanded text of the view, if the table is a view\. Otherwise it's `null`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`StorageDescriptor`  
Information about the physical storage of the table\.  
 *Required*: No  
 *Type*:   
 *Update requires*: No interruption 

`PartitionKeys`  
The columns in the table\.  
 *Required*: No  
 *Type*: List of   
 *Update requires*: No interruption 

`Retention`  
The retention time for the table\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: No interruption 

`Name`  
The name of the table\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 