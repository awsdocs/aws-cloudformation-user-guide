# AWS::Glue::Table Order<a name="aws-properties-glue-table-order"></a>

Specifies the sort order of a sorted column\.

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

`Column`  <a name="cfn-glue-table-order-column"></a>
The name of the column\.  
*Required*: Yes  
*Type*: [String](aws-properties-glue-table-column.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortOrder`  <a name="cfn-glue-table-order-sortorder"></a>
Indicates that the column is sorted in ascending order \(`== 1`\), or in descending order \(`==0`\)\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-glue-table-order--seealso"></a>
+  [Order Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Order) in the *AWS Glue Developer Guide* 

