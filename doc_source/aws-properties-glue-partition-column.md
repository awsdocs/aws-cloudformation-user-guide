# AWS Glue Partition Column<a name="aws-properties-glue-partition-column"></a>

<a name="aws-properties-glue-partition-column-description"></a>The `Column` property type specifies a column for an AWS Glue partition\.

<a name="aws-properties-glue-partition-column-inheritance"></a> The `Columns` property of the [AWS Glue Partition StorageDescriptor](aws-properties-glue-partition-storagedescriptor.md) property type contains a list of `Column` property types\.

## Syntax<a name="aws-properties-glue-partition-column-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-column-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-column-comment)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-column-type)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-column-name)" : String
}
```

### YAML<a name="aws-properties-glue-partition-column-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-column-comment): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-column-type): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-column-name): String
```

## Properties<a name="aws-properties-glue-partition-column-properties"></a>

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