# AWS::Glue::Table StorageDescriptor<a name="aws-properties-glue-table-storagedescriptor"></a>

Describes the physical storage of table data\.

## Syntax<a name="aws-properties-glue-table-storagedescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-storagedescriptor-syntax.json"></a>

```
{
  "[BucketColumns](#cfn-glue-table-storagedescriptor-bucketcolumns)" : [ String, ... ],
  "[Columns](#cfn-glue-table-storagedescriptor-columns)" : [ Column, ... ],
  "[Compressed](#cfn-glue-table-storagedescriptor-compressed)" : Boolean,
  "[InputFormat](#cfn-glue-table-storagedescriptor-inputformat)" : String,
  "[Location](#cfn-glue-table-storagedescriptor-location)" : String,
  "[NumberOfBuckets](#cfn-glue-table-storagedescriptor-numberofbuckets)" : Integer,
  "[OutputFormat](#cfn-glue-table-storagedescriptor-outputformat)" : String,
  "[Parameters](#cfn-glue-table-storagedescriptor-parameters)" : Json,
  "[SchemaReference](#cfn-glue-table-storagedescriptor-schemareference)" : SchemaReference,
  "[SerdeInfo](#cfn-glue-table-storagedescriptor-serdeinfo)" : SerdeInfo,
  "[SkewedInfo](#cfn-glue-table-storagedescriptor-skewedinfo)" : SkewedInfo,
  "[SortColumns](#cfn-glue-table-storagedescriptor-sortcolumns)" : [ Order, ... ],
  "[StoredAsSubDirectories](#cfn-glue-table-storagedescriptor-storedassubdirectories)" : Boolean
}
```

### YAML<a name="aws-properties-glue-table-storagedescriptor-syntax.yaml"></a>

```
  [BucketColumns](#cfn-glue-table-storagedescriptor-bucketcolumns): 
    - String
  [Columns](#cfn-glue-table-storagedescriptor-columns): 
    - Column
  [Compressed](#cfn-glue-table-storagedescriptor-compressed): Boolean
  [InputFormat](#cfn-glue-table-storagedescriptor-inputformat): String
  [Location](#cfn-glue-table-storagedescriptor-location): String
  [NumberOfBuckets](#cfn-glue-table-storagedescriptor-numberofbuckets): Integer
  [OutputFormat](#cfn-glue-table-storagedescriptor-outputformat): String
  [Parameters](#cfn-glue-table-storagedescriptor-parameters): Json
  [SchemaReference](#cfn-glue-table-storagedescriptor-schemareference): 
    SchemaReference
  [SerdeInfo](#cfn-glue-table-storagedescriptor-serdeinfo): 
    SerdeInfo
  [SkewedInfo](#cfn-glue-table-storagedescriptor-skewedinfo): 
    SkewedInfo
  [SortColumns](#cfn-glue-table-storagedescriptor-sortcolumns): 
    - Order
  [StoredAsSubDirectories](#cfn-glue-table-storagedescriptor-storedassubdirectories): Boolean
```

## Properties<a name="aws-properties-glue-table-storagedescriptor-properties"></a>

`BucketColumns`  <a name="cfn-glue-table-storagedescriptor-bucketcolumns"></a>
A list of reducer grouping columns, clustering columns, and bucketing columns in the table\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Columns`  <a name="cfn-glue-table-storagedescriptor-columns"></a>
A list of the `Columns` in the table\.  
*Required*: No  
*Type*: List of [Column](aws-properties-glue-table-column.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Compressed`  <a name="cfn-glue-table-storagedescriptor-compressed"></a>
 `True` if the data in the table is compressed, or `False` if not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputFormat`  <a name="cfn-glue-table-storagedescriptor-inputformat"></a>
The input format: `SequenceFileInputFormat` \(binary\), or `TextInputFormat`, or a custom format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Location`  <a name="cfn-glue-table-storagedescriptor-location"></a>
The physical location of the table\. By default, this takes the form of the warehouse location, followed by the database location in the warehouse, followed by the table name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfBuckets`  <a name="cfn-glue-table-storagedescriptor-numberofbuckets"></a>
Must be specified if the table contains any dimension columns\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputFormat`  <a name="cfn-glue-table-storagedescriptor-outputformat"></a>
The output format: `SequenceFileOutputFormat` \(binary\), or `IgnoreKeyTextOutputFormat`, or a custom format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-glue-table-storagedescriptor-parameters"></a>
The user\-supplied properties in key\-value form\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaReference`  <a name="cfn-glue-table-storagedescriptor-schemareference"></a>
An object that references a schema stored in the AWS Glue Schema Registry\.  
When creating a table, you can pass an empty list of columns for the schema, and instead use a schema reference\.  
*Required*: No  
*Type*: [SchemaReference](aws-properties-glue-table-schemareference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SerdeInfo`  <a name="cfn-glue-table-storagedescriptor-serdeinfo"></a>
The serialization/deserialization \(SerDe\) information\.  
*Required*: No  
*Type*: [SerdeInfo](aws-properties-glue-table-serdeinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SkewedInfo`  <a name="cfn-glue-table-storagedescriptor-skewedinfo"></a>
The information about values that appear frequently in a column \(skewed values\)\.  
*Required*: No  
*Type*: [SkewedInfo](aws-properties-glue-table-skewedinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortColumns`  <a name="cfn-glue-table-storagedescriptor-sortcolumns"></a>
A list specifying the sort order of each bucket in the table\.  
*Required*: No  
*Type*: List of [Order](aws-properties-glue-table-order.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StoredAsSubDirectories`  <a name="cfn-glue-table-storagedescriptor-storedassubdirectories"></a>
 `True` if the table data is stored in subdirectories, or `False` if not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-glue-table-storagedescriptor--seealso"></a>
+  [StorageDescriptor Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-StorageDescriptor) in the *AWS Glue Developer Guide* 

