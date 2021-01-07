# AWS::Glue::Partition StorageDescriptor<a name="aws-properties-glue-partition-storagedescriptor"></a>

Describes the physical storage of table data\.

## Syntax<a name="aws-properties-glue-partition-storagedescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-storagedescriptor-syntax.json"></a>

```
{
  "[BucketColumns](#cfn-glue-partition-storagedescriptor-bucketcolumns)" : [ String, ... ],
  "[Columns](#cfn-glue-partition-storagedescriptor-columns)" : [ Column, ... ],
  "[Compressed](#cfn-glue-partition-storagedescriptor-compressed)" : Boolean,
  "[InputFormat](#cfn-glue-partition-storagedescriptor-inputformat)" : String,
  "[Location](#cfn-glue-partition-storagedescriptor-location)" : String,
  "[NumberOfBuckets](#cfn-glue-partition-storagedescriptor-numberofbuckets)" : Integer,
  "[OutputFormat](#cfn-glue-partition-storagedescriptor-outputformat)" : String,
  "[Parameters](#cfn-glue-partition-storagedescriptor-parameters)" : Json,
  "[SchemaReference](#cfn-glue-partition-storagedescriptor-schemareference)" : SchemaReference,
  "[SerdeInfo](#cfn-glue-partition-storagedescriptor-serdeinfo)" : SerdeInfo,
  "[SkewedInfo](#cfn-glue-partition-storagedescriptor-skewedinfo)" : SkewedInfo,
  "[SortColumns](#cfn-glue-partition-storagedescriptor-sortcolumns)" : [ Order, ... ],
  "[StoredAsSubDirectories](#cfn-glue-partition-storagedescriptor-storedassubdirectories)" : Boolean
}
```

### YAML<a name="aws-properties-glue-partition-storagedescriptor-syntax.yaml"></a>

```
  [BucketColumns](#cfn-glue-partition-storagedescriptor-bucketcolumns): 
    - String
  [Columns](#cfn-glue-partition-storagedescriptor-columns): 
    - Column
  [Compressed](#cfn-glue-partition-storagedescriptor-compressed): Boolean
  [InputFormat](#cfn-glue-partition-storagedescriptor-inputformat): String
  [Location](#cfn-glue-partition-storagedescriptor-location): String
  [NumberOfBuckets](#cfn-glue-partition-storagedescriptor-numberofbuckets): Integer
  [OutputFormat](#cfn-glue-partition-storagedescriptor-outputformat): String
  [Parameters](#cfn-glue-partition-storagedescriptor-parameters): Json
  [SchemaReference](#cfn-glue-partition-storagedescriptor-schemareference): 
    SchemaReference
  [SerdeInfo](#cfn-glue-partition-storagedescriptor-serdeinfo): 
    SerdeInfo
  [SkewedInfo](#cfn-glue-partition-storagedescriptor-skewedinfo): 
    SkewedInfo
  [SortColumns](#cfn-glue-partition-storagedescriptor-sortcolumns): 
    - Order
  [StoredAsSubDirectories](#cfn-glue-partition-storagedescriptor-storedassubdirectories): Boolean
```

## Properties<a name="aws-properties-glue-partition-storagedescriptor-properties"></a>

`BucketColumns`  <a name="cfn-glue-partition-storagedescriptor-bucketcolumns"></a>
A list of reducer grouping columns, clustering columns, and bucketing columns in the table\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Columns`  <a name="cfn-glue-partition-storagedescriptor-columns"></a>
A list of the `Columns` in the table\.  
*Required*: No  
*Type*: List of [Column](aws-properties-glue-partition-column.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Compressed`  <a name="cfn-glue-partition-storagedescriptor-compressed"></a>
 `True` if the data in the table is compressed, or `False` if not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputFormat`  <a name="cfn-glue-partition-storagedescriptor-inputformat"></a>
The input format: `SequenceFileInputFormat` \(binary\), or `TextInputFormat`, or a custom format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Location`  <a name="cfn-glue-partition-storagedescriptor-location"></a>
The physical location of the table\. By default, this takes the form of the warehouse location, followed by the database location in the warehouse, followed by the table name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfBuckets`  <a name="cfn-glue-partition-storagedescriptor-numberofbuckets"></a>
The number of buckets\.  
You must specify this property if the partition contains any dimension columns\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputFormat`  <a name="cfn-glue-partition-storagedescriptor-outputformat"></a>
The output format: `SequenceFileOutputFormat` \(binary\), or `IgnoreKeyTextOutputFormat`, or a custom format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-glue-partition-storagedescriptor-parameters"></a>
The user\-supplied properties in key\-value form\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaReference`  <a name="cfn-glue-partition-storagedescriptor-schemareference"></a>
An object that references a schema stored in the AWS Glue Schema Registry\.  
When creating a table, you can pass an empty list of columns for the schema, and instead use a schema reference\.  
*Required*: No  
*Type*: [SchemaReference](aws-properties-glue-partition-schemareference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SerdeInfo`  <a name="cfn-glue-partition-storagedescriptor-serdeinfo"></a>
The serialization/deserialization \(SerDe\) information\.  
*Required*: No  
*Type*: [SerdeInfo](aws-properties-glue-partition-serdeinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SkewedInfo`  <a name="cfn-glue-partition-storagedescriptor-skewedinfo"></a>
The information about values that appear frequently in a column \(skewed values\)\.  
*Required*: No  
*Type*: [SkewedInfo](aws-properties-glue-partition-skewedinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortColumns`  <a name="cfn-glue-partition-storagedescriptor-sortcolumns"></a>
A list specifying the sort order of each bucket in the table\.  
*Required*: No  
*Type*: List of [Order](aws-properties-glue-partition-order.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StoredAsSubDirectories`  <a name="cfn-glue-partition-storagedescriptor-storedassubdirectories"></a>
 `True` if the table data is stored in subdirectories, or `False` if not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)