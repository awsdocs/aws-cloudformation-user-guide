# AWS::KinesisFirehose::DeliveryStream OrcSerDe<a name="aws-properties-kinesisfirehose-deliverystream-orcserde"></a>

A serializer to use for converting data to the ORC format before storing it in Amazon S3\. For more information, see [Apache ORC](https://orc.apache.org/docs/)\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-orcserde-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-orcserde-syntax.json"></a>

```
{
  "[BlockSizeBytes](#cfn-kinesisfirehose-deliverystream-orcserde-blocksizebytes)" : Integer,
  "[BloomFilterColumns](#cfn-kinesisfirehose-deliverystream-orcserde-bloomfiltercolumns)" : [ String, ... ],
  "[BloomFilterFalsePositiveProbability](#cfn-kinesisfirehose-deliverystream-orcserde-bloomfilterfalsepositiveprobability)" : Double,
  "[Compression](#cfn-kinesisfirehose-deliverystream-orcserde-compression)" : String,
  "[DictionaryKeyThreshold](#cfn-kinesisfirehose-deliverystream-orcserde-dictionarykeythreshold)" : Double,
  "[EnablePadding](#cfn-kinesisfirehose-deliverystream-orcserde-enablepadding)" : Boolean,
  "[FormatVersion](#cfn-kinesisfirehose-deliverystream-orcserde-formatversion)" : String,
  "[PaddingTolerance](#cfn-kinesisfirehose-deliverystream-orcserde-paddingtolerance)" : Double,
  "[RowIndexStride](#cfn-kinesisfirehose-deliverystream-orcserde-rowindexstride)" : Integer,
  "[StripeSizeBytes](#cfn-kinesisfirehose-deliverystream-orcserde-stripesizebytes)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-orcserde-syntax.yaml"></a>

```
  [BlockSizeBytes](#cfn-kinesisfirehose-deliverystream-orcserde-blocksizebytes): Integer
  [BloomFilterColumns](#cfn-kinesisfirehose-deliverystream-orcserde-bloomfiltercolumns): 
    - String
  [BloomFilterFalsePositiveProbability](#cfn-kinesisfirehose-deliverystream-orcserde-bloomfilterfalsepositiveprobability): Double
  [Compression](#cfn-kinesisfirehose-deliverystream-orcserde-compression): String
  [DictionaryKeyThreshold](#cfn-kinesisfirehose-deliverystream-orcserde-dictionarykeythreshold): Double
  [EnablePadding](#cfn-kinesisfirehose-deliverystream-orcserde-enablepadding): Boolean
  [FormatVersion](#cfn-kinesisfirehose-deliverystream-orcserde-formatversion): String
  [PaddingTolerance](#cfn-kinesisfirehose-deliverystream-orcserde-paddingtolerance): Double
  [RowIndexStride](#cfn-kinesisfirehose-deliverystream-orcserde-rowindexstride): Integer
  [StripeSizeBytes](#cfn-kinesisfirehose-deliverystream-orcserde-stripesizebytes): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-orcserde-properties"></a>

`BlockSizeBytes`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-blocksizebytes"></a>
The Hadoop Distributed File System \(HDFS\) block size\. This is useful if you intend to copy the data from Amazon S3 to HDFS before querying\. The default is 256 MiB and the minimum is 64 MiB\. Kinesis Data Firehose uses this value for padding calculations\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `67108864`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BloomFilterColumns`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-bloomfiltercolumns"></a>
The column names for which you want Kinesis Data Firehose to create bloom filters\. The default is `null`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BloomFilterFalsePositiveProbability`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-bloomfilterfalsepositiveprobability"></a>
The Bloom filter false positive probability \(FPP\)\. The lower the FPP, the bigger the Bloom filter\. The default value is 0\.05, the minimum is 0, and the maximum is 1\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Compression`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-compression"></a>
The compression code to use over data blocks\. The default is `SNAPPY`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | SNAPPY | ZLIB`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DictionaryKeyThreshold`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-dictionarykeythreshold"></a>
Represents the fraction of the total number of non\-null rows\. To turn off dictionary encoding, set this fraction to a number that is less than the number of distinct keys in a dictionary\. To always use dictionary encoding, set this threshold to 1\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnablePadding`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-enablepadding"></a>
Set this to `true` to indicate that you want stripes to be padded to the HDFS block boundaries\. This is useful if you intend to copy the data from Amazon S3 to HDFS before querying\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatVersion`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-formatversion"></a>
The version of the file to write\. The possible values are `V0_11` and `V0_12`\. The default is `V0_12`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `V0_11 | V0_12`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaddingTolerance`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-paddingtolerance"></a>
A number between 0 and 1 that defines the tolerance for block padding as a decimal fraction of stripe size\. The default value is 0\.05, which means 5 percent of stripe size\.  
For the default values of 64 MiB ORC stripes and 256 MiB HDFS blocks, the default block padding tolerance of 5 percent reserves a maximum of 3\.2 MiB for padding within the 256 MiB block\. In such a case, if the available size within the block is more than 3\.2 MiB, a new, smaller stripe is inserted to fit within that space\. This ensures that no stripe crosses block boundaries and causes remote reads within a node\-local task\.  
Kinesis Data Firehose ignores this parameter when `EnablePadding` is `false`\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowIndexStride`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-rowindexstride"></a>
The number of rows between index entries\. The default is 10,000 and the minimum is 1,000\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StripeSizeBytes`  <a name="cfn-kinesisfirehose-deliverystream-orcserde-stripesizebytes"></a>
The number of bytes in each stripe\. The default is 64 MiB and the minimum is 8 MiB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `8388608`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)