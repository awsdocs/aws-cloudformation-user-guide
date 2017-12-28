# Amazon Kinesis Firehose DeliveryStream ElasticsearchBufferingHints<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints"></a>

The `ElasticsearchBufferingHints` property type specifies how Amazon Kinesis Firehose \(Kinesis Firehose\) buffers incoming data while delivering it to the destination\. The first buffer condition that is satisfied triggers Kinesis Firehose to deliver the data\.

`ElasticsearchBufferingHints` is the property type for the `BufferingHints` property of the [Amazon Kinesis Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md) property type\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-intervalinseconds)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-sizeinmbs)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-intervalinseconds): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-sizeinmbs): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-properties"></a>

`IntervalInSeconds`  
The length of time, in seconds, that Kinesis Firehose buffers incoming data before delivering it to the destination\. For valid values, see the `IntervalInSeconds` content for the [BufferingHints](http://docs.aws.amazon.com/firehose/latest/APIReference/API_BufferingHints.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required: *Yes  
*Type*: Integer

`SizeInMBs`  
The size of the buffer, in MBs, that Kinesis Firehose uses for incoming data before delivering it to the destination\. For valid values, see the `SizeInMBs` content for the [BufferingHints](http://docs.aws.amazon.com/firehose/latest/APIReference/API_BufferingHints.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required: *Yes  
*Type*: Integer