# AWS::KinesisFirehose::DeliveryStream ParquetSerDe<a name="aws-properties-kinesisfirehose-deliverystream-parquetserde"></a>

A serializer to use for converting data to the Parquet format before storing it in Amazon S3\. For more information, see [Apache Parquet](https://parquet.apache.org/documentation/latest/)\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-parquetserde-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-parquetserde-syntax.json"></a>

```
{
  "[BlockSizeBytes](#cfn-kinesisfirehose-deliverystream-parquetserde-blocksizebytes)" : Integer,
  "[Compression](#cfn-kinesisfirehose-deliverystream-parquetserde-compression)" : String,
  "[EnableDictionaryCompression](#cfn-kinesisfirehose-deliverystream-parquetserde-enabledictionarycompression)" : Boolean,
  "[MaxPaddingBytes](#cfn-kinesisfirehose-deliverystream-parquetserde-maxpaddingbytes)" : Integer,
  "[PageSizeBytes](#cfn-kinesisfirehose-deliverystream-parquetserde-pagesizebytes)" : Integer,
  "[WriterVersion](#cfn-kinesisfirehose-deliverystream-parquetserde-writerversion)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-parquetserde-syntax.yaml"></a>

```
  [BlockSizeBytes](#cfn-kinesisfirehose-deliverystream-parquetserde-blocksizebytes): Integer
  [Compression](#cfn-kinesisfirehose-deliverystream-parquetserde-compression): String
  [EnableDictionaryCompression](#cfn-kinesisfirehose-deliverystream-parquetserde-enabledictionarycompression): Boolean
  [MaxPaddingBytes](#cfn-kinesisfirehose-deliverystream-parquetserde-maxpaddingbytes): Integer
  [PageSizeBytes](#cfn-kinesisfirehose-deliverystream-parquetserde-pagesizebytes): Integer
  [WriterVersion](#cfn-kinesisfirehose-deliverystream-parquetserde-writerversion): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-parquetserde-properties"></a>

`BlockSizeBytes`  <a name="cfn-kinesisfirehose-deliverystream-parquetserde-blocksizebytes"></a>
The Hadoop Distributed File System \(HDFS\) block size\. This is useful if you intend to copy the data from Amazon S3 to HDFS before querying\. The default is 256 MiB and the minimum is 64 MiB\. Kinesis Data Firehose uses this value for padding calculations\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `67108864`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Compression`  <a name="cfn-kinesisfirehose-deliverystream-parquetserde-compression"></a>
The compression code to use over data blocks\. The possible values are `UNCOMPRESSED`, `SNAPPY`, and `GZIP`, with the default being `SNAPPY`\. Use `SNAPPY` for higher decompression speed\. Use `GZIP` if the compression ratio is more important than speed\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GZIP | SNAPPY | UNCOMPRESSED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableDictionaryCompression`  <a name="cfn-kinesisfirehose-deliverystream-parquetserde-enabledictionarycompression"></a>
Indicates whether to enable dictionary compression\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxPaddingBytes`  <a name="cfn-kinesisfirehose-deliverystream-parquetserde-maxpaddingbytes"></a>
The maximum amount of padding to apply\. This is useful if you intend to copy the data from Amazon S3 to HDFS before querying\. The default is 0\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PageSizeBytes`  <a name="cfn-kinesisfirehose-deliverystream-parquetserde-pagesizebytes"></a>
The Parquet page size\. Column chunks are divided into pages\. A page is conceptually an indivisible unit \(in terms of compression and encoding\)\. The minimum value is 64 KiB and the default is 1 MiB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `65536`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriterVersion`  <a name="cfn-kinesisfirehose-deliverystream-parquetserde-writerversion"></a>
Indicates the version of row format to output\. The possible values are `V1` and `V2`\. The default is `V1`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `V1 | V2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)