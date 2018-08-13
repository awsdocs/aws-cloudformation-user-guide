# AWS Glue Table Order<a name="aws-properties-glue-table-order"></a>

<a name="aws-properties-glue-table-order-description"></a>The `Order` property type specifies the sort order of a column in an AWS Glue table\.

<a name="aws-properties-glue-table-order-inheritance"></a> The `SortColumns` property of the [AWS Glue Table StorageDescriptor](aws-properties-glue-table-storagedescriptor.md) property type contains a list of `Order` property types\.

## Syntax<a name="aws-properties-glue-table-order-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-order-syntax.json"></a>

```
{
  "[Column](#cfn-glue-table-order-column)" : String,
  "[SortOrder](#cfn-glue-table-order-sortorder)" : Integer
}
```

### YAML<a name="aws-properties-glue-table-order-syntax.yaml"></a>

```
[Column](#cfn-glue-table-order-column): String
[SortOrder](#cfn-glue-table-order-sortorder): Integer
```

## Properties<a name="aws-properties-glue-table-order-properties"></a>

For more information, see [Order Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Order) in the *AWS Glue Developer Guide*\.

`Column`  <a name="cfn-glue-table-order-column"></a>
The name of the column\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SortOrder`  <a name="cfn-glue-table-order-sortorder"></a>
Indicates whether the column is sorted in ascending order \(`1`\) or descending order \(`0`\)\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-table-order-seealso"></a>
+ [Order Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Order) in the *AWS Glue Developer Guide*