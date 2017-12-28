# AWS Glue Partition StorageDescriptor<a name="aws-properties-glue-partition-storagedescriptor"></a>

<a name="aws-properties-glue-partition-storagedescriptor-description"></a>The `StorageDescriptor` property type describes the physical storage of AWS Glue partition data\.

<a name="aws-properties-glue-partition-storagedescriptor-inheritance"></a> `StorageDescriptor` is a property of the [AWS Glue Partition PartitionInput](aws-properties-glue-partition-partitioninput.md) property type\.

## Syntax<a name="aws-properties-glue-partition-storagedescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-storagedescriptor-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-storedassubdirectories)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-parameters)" : JSON object,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-bucketcolumns)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-skewedinfo)" : SkewedInfo,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-inputformat)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-numberofbuckets)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-outputformat)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-columns)" : [ Column, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-serdeinfo)" : SerdeInfo,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-sortcolumns)" : [ Order, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-compressed)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-location)" : String
}
```

### YAML<a name="aws-properties-glue-partition-storagedescriptor-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-storedassubdirectories): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-parameters): 
  JSON object
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-bucketcolumns): 
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-skewedinfo): 
  SkewedInfo
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-inputformat): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-numberofbuckets): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-outputformat): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-columns): 
  - Column
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-serdeinfo): 
  SerdeInfo
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-sortcolumns): 
  - Order
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-compressed): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-partition-storagedescriptor-location): String
```

## Properties<a name="aws-properties-glue-partition-storagedescriptor-properties"></a>

`StoredAsSubDirectories`  
Indicates whether the partition data is stored in subdirectories\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Parameters`  
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify user\-supplied properties\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`BucketColumns`  
A list of UTF\-8 strings that specify reducer grouping columns, clustering columns, and bucketing columns in the partition\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 

`SkewedInfo`  
Information about values that appear very frequently in a column \(skewed values\)\.  
 *Required*: No  
 *Type*: [AWS Glue Partition SkewedInfo](aws-properties-glue-partition-skewedinfo.md)  
 *Update requires*: No interruption 

`InputFormat`  
The input format: `SequenceFileInputFormat` \(binary\), `TextInputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`NumberOfBuckets`  
The number of buckets\.  
 *Required*: Conditional\. You must specify this property if the partition contains any dimension columns\.  
 *Type*: Integer  
 *Update requires*: No interruption 

`OutputFormat`  
The output format: `SequenceFileOutputFormat` \(binary\), `IgnoreKeyTextOutputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Columns`  
The columns in the partition\.  
 *Required*: No  
 *Type*: List of [AWS Glue Partition Column](aws-properties-glue-partition-column.md)  
 *Update requires*: No interruption 

`SerdeInfo`  
Information about a serialization/deserialization program \(SerDe\), which serves as an extractor and loader\.  
 *Required*: No  
 *Type*: [AWS Glue Partition SerdeInfo](aws-properties-glue-partition-serdeinfo.md)  
 *Update requires*: No interruption 

`SortColumns`  
The sort order of each bucket in the partition\.  
 *Required*: No  
 *Type*: List of [AWS Glue Partition Order](aws-properties-glue-partition-order.md)  
 *Update requires*: No interruption 

`Compressed`  
Indicates whether the data in the partition is compressed\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Location`  
The physical location of the partition\. By default, this takes the form of the warehouse location, followed by the database location in the warehouse, followed by the partition name\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 