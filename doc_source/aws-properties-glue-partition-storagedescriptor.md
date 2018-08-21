# AWS Glue Partition StorageDescriptor<a name="aws-properties-glue-partition-storagedescriptor"></a>

<a name="aws-properties-glue-partition-storagedescriptor-description"></a>The `StorageDescriptor` property type describes the physical storage of AWS Glue partition data\.

<a name="aws-properties-glue-partition-storagedescriptor-inheritance"></a> `StorageDescriptor` is a property of the [AWS Glue Partition PartitionInput](aws-properties-glue-partition-partitioninput.md) property type\.

## Syntax<a name="aws-properties-glue-partition-storagedescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-storagedescriptor-syntax.json"></a>

```
{
  "[StoredAsSubDirectories](#cfn-glue-partition-storagedescriptor-storedassubdirectories)" : Boolean,
  "[Parameters](#cfn-glue-partition-storagedescriptor-parameters)" : JSON object,
  "[BucketColumns](#cfn-glue-partition-storagedescriptor-bucketcolumns)" : [ String, ... ],
  "[SkewedInfo](#cfn-glue-partition-storagedescriptor-skewedinfo)" : [*SkewedInfo*](aws-properties-glue-partition-skewedinfo.md),
  "[InputFormat](#cfn-glue-partition-storagedescriptor-inputformat)" : String,
  "[NumberOfBuckets](#cfn-glue-partition-storagedescriptor-numberofbuckets)" : Integer,
  "[OutputFormat](#cfn-glue-partition-storagedescriptor-outputformat)" : String,
  "[Columns](#cfn-glue-partition-storagedescriptor-columns)" : [ [*Column*](aws-properties-glue-partition-column.md), ... ],
  "[SerdeInfo](#cfn-glue-partition-storagedescriptor-serdeinfo)" : [*SerdeInfo*](aws-properties-glue-partition-serdeinfo.md),
  "[SortColumns](#cfn-glue-partition-storagedescriptor-sortcolumns)" : [ [*Order*](aws-properties-glue-partition-order.md), ... ],
  "[Compressed](#cfn-glue-partition-storagedescriptor-compressed)" : Boolean,
  "[Location](#cfn-glue-partition-storagedescriptor-location)" : String
}
```

### YAML<a name="aws-properties-glue-partition-storagedescriptor-syntax.yaml"></a>

```
[StoredAsSubDirectories](#cfn-glue-partition-storagedescriptor-storedassubdirectories): Boolean
[Parameters](#cfn-glue-partition-storagedescriptor-parameters): 
  JSON object
[BucketColumns](#cfn-glue-partition-storagedescriptor-bucketcolumns): 
  - String
[SkewedInfo](#cfn-glue-partition-storagedescriptor-skewedinfo): 
  [*SkewedInfo*](aws-properties-glue-partition-skewedinfo.md)
[InputFormat](#cfn-glue-partition-storagedescriptor-inputformat): String
[NumberOfBuckets](#cfn-glue-partition-storagedescriptor-numberofbuckets): Integer
[OutputFormat](#cfn-glue-partition-storagedescriptor-outputformat): String
[Columns](#cfn-glue-partition-storagedescriptor-columns): 
  - [*Column*](aws-properties-glue-partition-column.md)
[SerdeInfo](#cfn-glue-partition-storagedescriptor-serdeinfo): 
  [*SerdeInfo*](aws-properties-glue-partition-serdeinfo.md)
[SortColumns](#cfn-glue-partition-storagedescriptor-sortcolumns): 
  - [*Order*](aws-properties-glue-partition-order.md)
[Compressed](#cfn-glue-partition-storagedescriptor-compressed): Boolean
[Location](#cfn-glue-partition-storagedescriptor-location): String
```

## Properties<a name="aws-properties-glue-partition-storagedescriptor-properties"></a>

`StoredAsSubDirectories`  <a name="cfn-glue-partition-storagedescriptor-storedassubdirectories"></a>
Indicates whether the partition data is stored in subdirectories\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Parameters`  <a name="cfn-glue-partition-storagedescriptor-parameters"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify user\-supplied properties\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`BucketColumns`  <a name="cfn-glue-partition-storagedescriptor-bucketcolumns"></a>
A list of UTF\-8 strings that specify reducer grouping columns, clustering columns, and bucketing columns in the partition\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SkewedInfo`  <a name="cfn-glue-partition-storagedescriptor-skewedinfo"></a>
Information about values that appear very frequently in a column \(skewed values\)\.  
 *Required*: No  
 *Type*: [AWS Glue Partition SkewedInfo](aws-properties-glue-partition-skewedinfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InputFormat`  <a name="cfn-glue-partition-storagedescriptor-inputformat"></a>
The input format: `SequenceFileInputFormat` \(binary\), `TextInputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NumberOfBuckets`  <a name="cfn-glue-partition-storagedescriptor-numberofbuckets"></a>
The number of buckets\.  
 *Required*: Conditional\. You must specify this property if the partition contains any dimension columns\.  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OutputFormat`  <a name="cfn-glue-partition-storagedescriptor-outputformat"></a>
The output format: `SequenceFileOutputFormat` \(binary\), `IgnoreKeyTextOutputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Columns`  <a name="cfn-glue-partition-storagedescriptor-columns"></a>
The columns in the partition\.  
 *Required*: No  
 *Type*: List of [AWS Glue Partition Column](aws-properties-glue-partition-column.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SerdeInfo`  <a name="cfn-glue-partition-storagedescriptor-serdeinfo"></a>
Information about a serialization/deserialization program \(SerDe\), which serves as an extractor and loader\.  
 *Required*: No  
 *Type*: [AWS Glue Partition SerdeInfo](aws-properties-glue-partition-serdeinfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SortColumns`  <a name="cfn-glue-partition-storagedescriptor-sortcolumns"></a>
The sort order of each bucket in the partition\.  
 *Required*: No  
 *Type*: List of [AWS Glue Partition Order](aws-properties-glue-partition-order.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Compressed`  <a name="cfn-glue-partition-storagedescriptor-compressed"></a>
Indicates whether the data in the partition is compressed\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Location`  <a name="cfn-glue-partition-storagedescriptor-location"></a>
The physical location of the partition\. By default, this takes the form of the warehouse location, followed by the database location in the warehouse, followed by the partition name\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 