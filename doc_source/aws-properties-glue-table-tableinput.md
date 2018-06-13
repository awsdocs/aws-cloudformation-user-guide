# AWS Glue Table TableInput<a name="aws-properties-glue-table-tableinput"></a>

<a name="aws-properties-glue-table-tableinput-description"></a>The `TableInput` property type specifies the metadata that's used to create or update an AWS Glue table\.

<a name="aws-properties-glue-table-tableinput-inheritance"></a> `TableInput` is a property of the [AWS::Glue::Table](aws-resource-glue-table.md) resource\.

## Syntax<a name="aws-properties-glue-table-tableinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-tableinput-syntax.json"></a>

```
{
  "[Owner](#cfn-glue-table-tableinput-owner)" : String,
  "[ViewOriginalText](#cfn-glue-table-tableinput-vieworiginaltext)" : String,
  "[Description](#cfn-glue-table-tableinput-description)" : String,
  "[TableType](#cfn-glue-table-tableinput-tabletype)" : String,
  "[Parameters](#cfn-glue-table-tableinput-parameters)" : JSON object,
  "[ViewExpandedText](#cfn-glue-table-tableinput-viewexpandedtext)" : String,
  "[StorageDescriptor](#cfn-glue-table-tableinput-storagedescriptor)" : [*StorageDescriptor*](aws-properties-glue-table-storagedescriptor.md),
  "[PartitionKeys](#cfn-glue-table-tableinput-partitionkeys)" : [ [*Column*](aws-properties-glue-table-column.md), ... ],
  "[Retention](#cfn-glue-table-tableinput-retention)" : Integer,
  "[Name](#cfn-glue-table-tableinput-name)" : String
}
```

### YAML<a name="aws-properties-glue-table-tableinput-syntax.yaml"></a>

```
[Owner](#cfn-glue-table-tableinput-owner): String
[ViewOriginalText](#cfn-glue-table-tableinput-vieworiginaltext): String
[Description](#cfn-glue-table-tableinput-description): String
[TableType](#cfn-glue-table-tableinput-tabletype): String
[Parameters](#cfn-glue-table-tableinput-parameters): JSON object
[ViewExpandedText](#cfn-glue-table-tableinput-viewexpandedtext): String
[StorageDescriptor](#cfn-glue-table-tableinput-storagedescriptor): 
  [*StorageDescriptor*](aws-properties-glue-table-storagedescriptor.md)
[PartitionKeys](#cfn-glue-table-tableinput-partitionkeys): 
  - [*Column*](aws-properties-glue-table-column.md)
[Retention](#cfn-glue-table-tableinput-retention): Integer
[Name](#cfn-glue-table-tableinput-name): String
```

## Properties<a name="aws-properties-glue-table-tableinput-properties"></a>

For more information, see [TableInput Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-TableInput) in the *AWS Glue Developer Guide*\.

`Owner`  <a name="cfn-glue-table-tableinput-owner"></a>
The owner of the table\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ViewOriginalText`  <a name="cfn-glue-table-tableinput-vieworiginaltext"></a>
The original text of the view, if the table is a view\. Otherwise, it's `null`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-glue-table-tableinput-description"></a>
The description of the table\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TableType`  <a name="cfn-glue-table-tableinput-tabletype"></a>
The type of the table, such as `EXTERNAL_TABLE` or `VIRTUAL_VIEW`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Parameters`  <a name="cfn-glue-table-tableinput-parameters"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the properties that are associated with the table\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ViewExpandedText`  <a name="cfn-glue-table-tableinput-viewexpandedtext"></a>
The expanded text of the view, if the table is a view\. Otherwise it's `null`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StorageDescriptor`  <a name="cfn-glue-table-tableinput-storagedescriptor"></a>
Information about the physical storage of the table\.  
 *Required*: No  
 *Type*: [AWS Glue Table StorageDescriptor](aws-properties-glue-table-storagedescriptor.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PartitionKeys`  <a name="cfn-glue-table-tableinput-partitionkeys"></a>
The columns in the table\.  
 *Required*: No  
 *Type*: List of [AWS Glue Table Column](aws-properties-glue-table-column.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Retention`  <a name="cfn-glue-table-tableinput-retention"></a>
The retention time for the table\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-table-tableinput-name"></a>
The name of the table\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 