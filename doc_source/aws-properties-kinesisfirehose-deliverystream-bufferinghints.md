# Amazon Kinesis Firehose DeliveryStream BufferingHints<a name="aws-properties-kinesisfirehose-deliverystream-bufferinghints"></a>

The `BufferingHints` property type specifies how Amazon Kinesis Firehose \(Kinesis Firehose\) buffers incoming data before delivering it to the destination\. The first buffer condition that is satisfied triggers Kinesis Firehose to deliver the data\.

`BufferingHints` is a property of the [Amazon Kinesis Firehose DeliveryStream ExtendedS3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.md) and [Amazon Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md) property types\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-bufferinghints-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-bufferinghints-syntax.json"></a>

```
{
  "[IntervalInSeconds](#cfn-kinesisfirehose-deliverystream-bufferinghints-intervalinseconds)" : Integer,
  "[SizeInMBs](#cfn-kinesisfirehose-deliverystream-bufferinghints-sizeinmbs)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-bufferinghints-syntax.yaml"></a>

```
[IntervalInSeconds](#cfn-kinesisfirehose-deliverystream-bufferinghints-intervalinseconds): Integer
[SizeInMBs](#cfn-kinesisfirehose-deliverystream-bufferinghints-sizeinmbs): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-bufferinghints-properties"></a>

`IntervalInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-bufferinghints-intervalinseconds"></a>
The length of time, in seconds, that Kinesis Firehose buffers incoming data before delivering it to the destination\. For valid values, see the `IntervalInSeconds` content for the [BufferingHints](http://docs.aws.amazon.com/firehose/latest/APIReference/API_BufferingHints.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required*: Yes  
*Type*: Integer

`SizeInMBs`  <a name="cfn-kinesisfirehose-deliverystream-bufferinghints-sizeinmbs"></a>
The size of the buffer, in MBs, that Kinesis Firehose uses for incoming data before delivering it to the destination\. For valid values, see the `SizeInMBs` content for the [BufferingHints](http://docs.aws.amazon.com/firehose/latest/APIReference/API_BufferingHints.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required*: Yes  
*Type*: Integer