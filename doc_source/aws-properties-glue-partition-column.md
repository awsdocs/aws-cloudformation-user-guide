# AWS Glue Partition Column<a name="aws-properties-glue-partition-column"></a>

<a name="aws-properties-glue-partition-column-description"></a>The `Column` property type specifies a column for an AWS Glue partition\.

<a name="aws-properties-glue-partition-column-inheritance"></a> The `Columns` property of the [AWS Glue Partition StorageDescriptor](aws-properties-glue-partition-storagedescriptor.md) property type contains a list of `Column` property types\.

## Syntax<a name="aws-properties-glue-partition-column-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-column-syntax.json"></a>

```
{
  "[Comment](#cfn-glue-partition-column-comment)" : String,
  "[Type](#cfn-glue-partition-column-type)" : String,
  "[Name](#cfn-glue-partition-column-name)" : String
}
```

### YAML<a name="aws-properties-glue-partition-column-syntax.yaml"></a>

```
[Comment](#cfn-glue-partition-column-comment): String
[Type](#cfn-glue-partition-column-type): String
[Name](#cfn-glue-partition-column-name): String
```

## Properties<a name="aws-properties-glue-partition-column-properties"></a>

`Comment`  <a name="cfn-glue-partition-column-comment"></a>
A free\-form text comment\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Type`  <a name="cfn-glue-partition-column-type"></a>
The data type of the column data\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-partition-column-name"></a>
The name of the column\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 