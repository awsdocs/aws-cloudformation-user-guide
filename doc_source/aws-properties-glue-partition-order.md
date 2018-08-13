# AWS Glue Partition Order<a name="aws-properties-glue-partition-order"></a>

<a name="aws-properties-glue-partition-order-description"></a>The `Order` property type specifies the sort order of a column in an AWS Glue partition\.

<a name="aws-properties-glue-partition-order-inheritance"></a> The `SortColumns` property of the [AWS Glue Partition StorageDescriptor](aws-properties-glue-partition-storagedescriptor.md) property type contains a list of `Order` property types\.

## Syntax<a name="aws-properties-glue-partition-order-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-order-syntax.json"></a>

```
{
  "[Column](#cfn-glue-partition-order-column)" : String,
  "[SortOrder](#cfn-glue-partition-order-sortorder)" : Integer
}
```

### YAML<a name="aws-properties-glue-partition-order-syntax.yaml"></a>

```
[Column](#cfn-glue-partition-order-column): String
[SortOrder](#cfn-glue-partition-order-sortorder): Integer
```

## Properties<a name="aws-properties-glue-partition-order-properties"></a>

`Column`  <a name="cfn-glue-partition-order-column"></a>
The name of the column\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SortOrder`  <a name="cfn-glue-partition-order-sortorder"></a>
Indicates whether the column is sorted in ascending order \(`1`\) or descending order \(`0`\)\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 