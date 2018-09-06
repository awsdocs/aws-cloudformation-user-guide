# AWS Glue Table StorageDescriptor<a name="aws-properties-glue-table-storagedescriptor"></a>

<a name="aws-properties-glue-table-storagedescriptor-description"></a>The `StorageDescriptor` property type describes the physical storage of AWS Glue table data\.

<a name="aws-properties-glue-table-storagedescriptor-inheritance"></a> `StorageDescriptor` is a property of the [AWS Glue Table TableInput](aws-properties-glue-table-tableinput.md) property type\.

## Syntax<a name="aws-properties-glue-table-storagedescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-storagedescriptor-syntax.json"></a>

```
{
  "[StoredAsSubDirectories](#cfn-glue-table-storagedescriptor-storedassubdirectories)" : Boolean,
  "[Parameters](#cfn-glue-table-storagedescriptor-parameters)" : JSON object,
  "[BucketColumns](#cfn-glue-table-storagedescriptor-bucketcolumns)" : [ String, ... ],
  "[SkewedInfo](#cfn-glue-table-storagedescriptor-skewedinfo)" : [*SkewedInfo*](aws-properties-glue-table-skewedinfo.md),
  "[InputFormat](#cfn-glue-table-storagedescriptor-inputformat)" : String,
  "[NumberOfBuckets](#cfn-glue-table-storagedescriptor-numberofbuckets)" : Integer,
  "[OutputFormat](#cfn-glue-table-storagedescriptor-outputformat)" : String,
  "[Columns](#cfn-glue-table-storagedescriptor-columns)" : [ [*Column*](aws-properties-glue-table-column.md), ... ],
  "[SerdeInfo](#cfn-glue-table-storagedescriptor-serdeinfo)" : [*SerdeInfo*](aws-properties-glue-table-serdeinfo.md),
  "[SortColumns](#cfn-glue-table-storagedescriptor-sortcolumns)" : [ [*Order*](aws-properties-glue-table-order.md), ... ],
  "[Compressed](#cfn-glue-table-storagedescriptor-compressed)" : Boolean,
  "[Location](#cfn-glue-table-storagedescriptor-location)" : String
}
```

### YAML<a name="aws-properties-glue-table-storagedescriptor-syntax.yaml"></a>

```
[StoredAsSubDirectories](#cfn-glue-table-storagedescriptor-storedassubdirectories): Boolean
[Parameters](#cfn-glue-table-storagedescriptor-parameters): JSON object
[BucketColumns](#cfn-glue-table-storagedescriptor-bucketcolumns): 
  - String
[SkewedInfo](#cfn-glue-table-storagedescriptor-skewedinfo): 
  [*SkewedInfo*](aws-properties-glue-table-skewedinfo.md)
[InputFormat](#cfn-glue-table-storagedescriptor-inputformat): String
[NumberOfBuckets](#cfn-glue-table-storagedescriptor-numberofbuckets): Integer
[OutputFormat](#cfn-glue-table-storagedescriptor-outputformat): String
[Columns](#cfn-glue-table-storagedescriptor-columns): 
  - [*Column*](aws-properties-glue-table-column.md)
[SerdeInfo](#cfn-glue-table-storagedescriptor-serdeinfo): 
  [*SerdeInfo*](aws-properties-glue-table-serdeinfo.md)
[SortColumns](#cfn-glue-table-storagedescriptor-sortcolumns): 
  - [*Order*](aws-properties-glue-table-order.md)
[Compressed](#cfn-glue-table-storagedescriptor-compressed): Boolean
[Location](#cfn-glue-table-storagedescriptor-location): String
```

## Properties<a name="aws-properties-glue-table-storagedescriptor-properties"></a>

For more information, see [StorageDescriptor Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-StorageDescriptor) in the *AWS Glue Developer Guide*\.

`StoredAsSubDirectories`  <a name="cfn-glue-table-storagedescriptor-storedassubdirectories"></a>
Indicates whether the table data is stored in subdirectories\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Parameters`  <a name="cfn-glue-table-storagedescriptor-parameters"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify user\-supplied properties\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`BucketColumns`  <a name="cfn-glue-table-storagedescriptor-bucketcolumns"></a>
A list of UTF\-8 strings that specify reducer grouping columns, clustering columns, and bucketing columns in the table\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SkewedInfo`  <a name="cfn-glue-table-storagedescriptor-skewedinfo"></a>
Information about values that appear very frequently in a column \(skewed values\)\.  
 *Required*: No  
 *Type*: [AWS Glue Table SkewedInfo](aws-properties-glue-table-skewedinfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InputFormat`  <a name="cfn-glue-table-storagedescriptor-inputformat"></a>
The input format: `SequenceFileInputFormat` \(binary\), `TextInputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NumberOfBuckets`  <a name="cfn-glue-table-storagedescriptor-numberofbuckets"></a>
The number of buckets\.  
 *Required*: Conditional\. You must specify this property if the table contains any dimension columns\.  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OutputFormat`  <a name="cfn-glue-table-storagedescriptor-outputformat"></a>
The output format: `SequenceFileOutputFormat` \(binary\), `IgnoreKeyTextOutputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Columns`  <a name="cfn-glue-table-storagedescriptor-columns"></a>
The columns in the table\.  
 *Required*: No  
 *Type*: List of [AWS Glue Table Column](aws-properties-glue-table-column.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SerdeInfo`  <a name="cfn-glue-table-storagedescriptor-serdeinfo"></a>
Information about a serialization/deserialization program \(SerDe\), which serves as an extractor and loader\.  
 *Required*: No  
 *Type*: [AWS Glue Table SerdeInfo](aws-properties-glue-table-serdeinfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SortColumns`  <a name="cfn-glue-table-storagedescriptor-sortcolumns"></a>
The sort order of each bucket in the table\.  
 *Required*: No  
 *Type*: List of [AWS Glue Table Order](aws-properties-glue-table-order.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Compressed`  <a name="cfn-glue-table-storagedescriptor-compressed"></a>
Indicates whether the data in the table is compressed\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Location`  <a name="cfn-glue-table-storagedescriptor-location"></a>
The physical location of the table\. By default, this takes the form of the warehouse location, followed by the database location in the warehouse, followed by the table name\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-table-storagedescriptor-seealso"></a>
+ [StorageDescriptor Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-StorageDescriptor) in the *AWS Glue Developer Guide*