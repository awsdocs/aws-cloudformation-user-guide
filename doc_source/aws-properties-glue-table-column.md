# AWS::Glue::Table Column<a name="aws-properties-glue-table-column"></a>

A column in a `Table`\.

## Syntax<a name="aws-properties-glue-table-column-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-column-syntax.json"></a>

```
{
  "[Comment](#cfn-glue-table-column-comment)" : String,
  "[Name](#cfn-glue-table-column-name)" : String,
  "[Type](#cfn-glue-table-column-type)" : String
}
```

### YAML<a name="aws-properties-glue-table-column-syntax.yaml"></a>

```
  [Comment](#cfn-glue-table-column-comment): String
  [Name](#cfn-glue-table-column-name): String
  [Type](#cfn-glue-table-column-type): String
```

## Properties<a name="aws-properties-glue-table-column-properties"></a>

`Comment`  <a name="cfn-glue-table-column-comment"></a>
A free\-form text comment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-table-column-name"></a>
The name of the `Column`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-glue-table-column-type"></a>
The data type of the `Column`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-glue-table-column--seealso"></a>
+  [Column Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Column) in the *AWS Glue Developer Guide* 

