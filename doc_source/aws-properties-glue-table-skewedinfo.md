# AWS Glue Table SkewedInfo<a name="aws-properties-glue-table-skewedinfo"></a>

<a name="aws-properties-glue-table-skewedinfo-description"></a>The `SkewedInfo` property type specifies skewed values \(values that occur with very high frequency\) in an AWS Glue table\.

<a name="aws-properties-glue-table-skewedinfo-inheritance"></a> `SkewedInfo` is a property of the [AWS Glue Table StorageDescriptor](aws-properties-glue-table-storagedescriptor.md) property type\.

## Syntax<a name="aws-properties-glue-table-skewedinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-skewedinfo-syntax.json"></a>

```
{
  "[SkewedColumnNames](#cfn-glue-table-skewedinfo-skewedcolumnnames)" : [ String, ... ],
  "[SkewedColumnValues](#cfn-glue-table-skewedinfo-skewedcolumnvalues)" : [ String, ... ],
  "[SkewedColumnValueLocationMaps](#cfn-glue-table-skewedinfo-skewedcolumnvaluelocationmaps)" : JSON object
}
```

### YAML<a name="aws-properties-glue-table-skewedinfo-syntax.yaml"></a>

```
[SkewedColumnNames](#cfn-glue-table-skewedinfo-skewedcolumnnames): 
  - String
[SkewedColumnValues](#cfn-glue-table-skewedinfo-skewedcolumnvalues): 
  - String
[SkewedColumnValueLocationMaps](#cfn-glue-table-skewedinfo-skewedcolumnvaluelocationmaps): JSON object
```

## Properties<a name="aws-properties-glue-table-skewedinfo-properties"></a>

For more information, see [SkewedInfo Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-SkewedInfo) in the *AWS Glue Developer Guide*\.

`SkewedColumnNames`  <a name="cfn-glue-table-skewedinfo-skewedcolumnnames"></a>
A list of UTF\-8 strings that specify the names of columns that contain skewed values\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SkewedColumnValues`  <a name="cfn-glue-table-skewedinfo-skewedcolumnvalues"></a>
A list of UTF\-8 strings that specify values that appear so frequently that they're considered to be skewed\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SkewedColumnValueLocationMaps`  <a name="cfn-glue-table-skewedinfo-skewedcolumnvaluelocationmaps"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that map skewed values to the columns that contain them\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-table-skewedinfo-seealso"></a>
+ [SkewedInfo Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-SkewedInfo) in the *AWS Glue Developer Guide*