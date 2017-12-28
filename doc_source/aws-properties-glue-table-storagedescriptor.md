# AWS Glue Table StorageDescriptor<a name="aws-properties-glue-table-storagedescriptor"></a>

<a name="aws-properties-glue-table-storagedescriptor-description"></a>The `StorageDescriptor` property type describes the physical storage of AWS Glue table data\.

<a name="aws-properties-glue-table-storagedescriptor-inheritance"></a> `StorageDescriptor` is a property of the [AWS Glue Table TableInput](aws-properties-glue-table-tableinput.md) property type\.

## Syntax<a name="aws-properties-glue-table-storagedescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-storagedescriptor-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-storedassubdirectories)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-parameters)" : JSON object,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-bucketcolumns)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-skewedinfo)" : SkewedInfo,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-inputformat)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-numberofbuckets)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-outputformat)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-columns)" : [ Column, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-serdeinfo)" : SerdeInfo,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-sortcolumns)" : [ Order, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-compressed)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-location)" : String
}
```

### YAML<a name="aws-properties-glue-table-storagedescriptor-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-storedassubdirectories): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-parameters): JSON object
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-bucketcolumns): 
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-skewedinfo): 
  SkewedInfo
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-inputformat): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-numberofbuckets): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-outputformat): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-columns): 
  - Column
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-serdeinfo): 
  SerdeInfo
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-sortcolumns): 
  - Order
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-compressed): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-storagedescriptor-location): String
```

## Properties<a name="aws-properties-glue-table-storagedescriptor-properties"></a>

For more information, see [StorageDescriptor Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-StorageDescriptor) in the *AWS Glue Developer Guide*\.

`StoredAsSubDirectories`  
Indicates whether the table data is stored in subdirectories\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Parameters`  
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify user\-supplied properties\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`BucketColumns`  
A list of UTF\-8 strings that specify reducer grouping columns, clustering columns, and bucketing columns in the table\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 

`SkewedInfo`  
Information about values that appear very frequently in a column \(skewed values\)\.  
 *Required*: No  
 *Type*:   
 *Update requires*: No interruption 

`InputFormat`  
The input format: `SequenceFileInputFormat` \(binary\), `TextInputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`NumberOfBuckets`  
The number of buckets\.  
 *Required*: Conditional\. You must specify this property if the table contains any dimension columns\.  
 *Type*: Integer  
 *Update requires*: No interruption 

`OutputFormat`  
The output format: `SequenceFileOutputFormat` \(binary\), `IgnoreKeyTextOutputFormat`, or a custom format\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Columns`  
The columns in the table\.  
 *Required*: No  
 *Type*: List of   
 *Update requires*: No interruption 

`SerdeInfo`  
Information about a serialization/deserialization program \(SerDe\), which serves as an extractor and loader\.  
 *Required*: No  
 *Type*:   
 *Update requires*: No interruption 

`SortColumns`  
The sort order of each bucket in the table\.  
 *Required*: No  
 *Type*: List of   
 *Update requires*: No interruption 

`Compressed`  
Indicates whether the data in the table is compressed\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Location`  
The physical location of the table\. By default, this takes the form of the warehouse location, followed by the database location in the warehouse, followed by the table name\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

## See Also<a name="aws-properties-glue-table-storagedescriptor-seealso"></a>

+ [StorageDescriptor Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-StorageDescriptor) in the *AWS Glue Developer Guide*