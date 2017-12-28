# AWS Glue Table Column<a name="aws-properties-glue-table-column"></a>

<a name="aws-properties-glue-table-column-description"></a>The `Column` property type specifies a column for an AWS Glue table\.

<a name="aws-properties-glue-table-column-inheritance"></a> The `PartitionKeys` property of the [AWS Glue Table TableInput](aws-properties-glue-table-tableinput.md) property type and the `Columns` property of the [AWS Glue Table StorageDescriptor](aws-properties-glue-table-storagedescriptor.md) property type contain a list of `Column` property types\.

## Syntax<a name="aws-properties-glue-table-column-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-column-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-column-comment)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-column-type)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-column-name)" : String
}
```

### YAML<a name="aws-properties-glue-table-column-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-column-comment): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-column-type): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-column-name): String
```

## Properties<a name="aws-properties-glue-table-column-properties"></a>

For more information, see [Column Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Column) in the *AWS Glue Developer Guide*\.

`Comment`  
A free\-form text comment\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Type`  
The data type of the column data\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Name`  
The name of the column\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

## See Also<a name="aws-properties-glue-table-column-seealso"></a>

+ [Column Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Column) in the *AWS Glue Developer Guide*