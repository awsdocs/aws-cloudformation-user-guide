# AWS Glue Table SerdeInfo<a name="aws-properties-glue-table-serdeinfo"></a>

<a name="aws-properties-glue-table-serdeinfo-description"></a>The `SerdeInfo` property type specifies information about a serialization/deserialization program \(SerDe\), which serves as an extractor and loader for an AWS Glue table\.

<a name="aws-properties-glue-table-serdeinfo-inheritance"></a> `SerdeInfo` is a property of the [AWS Glue Table StorageDescriptor](aws-properties-glue-table-storagedescriptor.md) property type\.

## Syntax<a name="aws-properties-glue-table-serdeinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-serdeinfo-syntax.json"></a>

```
{
  "[Parameters](#cfn-glue-table-serdeinfo-parameters)" : JSON object,
  "[SerializationLibrary](#cfn-glue-table-serdeinfo-serializationlibrary)" : String,
  "[Name](#cfn-glue-table-serdeinfo-name)" : String
}
```

### YAML<a name="aws-properties-glue-table-serdeinfo-syntax.yaml"></a>

```
[Parameters](#cfn-glue-table-serdeinfo-parameters): JSON object
[SerializationLibrary](#cfn-glue-table-serdeinfo-serializationlibrary): String
[Name](#cfn-glue-table-serdeinfo-name): String
```

## Properties<a name="aws-properties-glue-table-serdeinfo-properties"></a>

For more information, see [SerDeInfo Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-SerDeInfo) in the *AWS Glue Developer Guide*\.

`Parameters`  <a name="cfn-glue-table-serdeinfo-parameters"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the initialization parameters for the SerDe\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SerializationLibrary`  <a name="cfn-glue-table-serdeinfo-serializationlibrary"></a>
The serialization library\. This is usually the class that implements the SerDe, such as `org.apache.hadoop.hive.serde2.columnar.ColumnarSerDe`\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-table-serdeinfo-name"></a>
The name of the SerDe\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-table-serdeinfo-seealso"></a>
+ [SerDeInfo Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-SerDeInfo) in the *AWS Glue Developer Guide*