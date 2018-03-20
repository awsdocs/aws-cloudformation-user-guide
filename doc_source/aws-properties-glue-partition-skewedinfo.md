# AWS Glue Partition SkewedInfo<a name="aws-properties-glue-partition-skewedinfo"></a>

<a name="aws-properties-glue-partition-skewedinfo-description"></a>The `SkewedInfo` property type specifies skewed values \(values that occur with very high frequency\) in an AWS Glue partition\.

<a name="aws-properties-glue-partition-skewedinfo-inheritance"></a> `SkewedInfo` is a property of the [AWS Glue Partition StorageDescriptor](aws-properties-glue-partition-storagedescriptor.md) property type\.

## Syntax<a name="aws-properties-glue-partition-skewedinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-skewedinfo-syntax.json"></a>

```
{
  "[SkewedColumnNames](#cfn-glue-partition-skewedinfo-skewedcolumnnames)" : [ String, ... ],
  "[SkewedColumnValues](#cfn-glue-partition-skewedinfo-skewedcolumnvalues)" : [ String, ... ],
  "[SkewedColumnValueLocationMaps](#cfn-glue-partition-skewedinfo-skewedcolumnvaluelocationmaps)" : JSON object
}
```

### YAML<a name="aws-properties-glue-partition-skewedinfo-syntax.yaml"></a>

```
[SkewedColumnNames](#cfn-glue-partition-skewedinfo-skewedcolumnnames): 
  - String
[SkewedColumnValues](#cfn-glue-partition-skewedinfo-skewedcolumnvalues): 
  - String
[SkewedColumnValueLocationMaps](#cfn-glue-partition-skewedinfo-skewedcolumnvaluelocationmaps):
  JSON object
```

## Properties<a name="aws-properties-glue-partition-skewedinfo-properties"></a>

`SkewedColumnNames`  <a name="cfn-glue-partition-skewedinfo-skewedcolumnnames"></a>
A list of UTF\-8 strings that specify the names of columns that contain skewed values\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SkewedColumnValues`  <a name="cfn-glue-partition-skewedinfo-skewedcolumnvalues"></a>
A list of UTF\-8 strings that specify values that appear so frequently that they're considered to be skewed\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SkewedColumnValueLocationMaps`  <a name="cfn-glue-partition-skewedinfo-skewedcolumnvaluelocationmaps"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that map skewed values to the columns that contain them\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 