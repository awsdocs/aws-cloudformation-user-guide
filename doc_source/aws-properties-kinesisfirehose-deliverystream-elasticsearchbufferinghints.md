# AWS::KinesisFirehose::DeliveryStream ElasticsearchBufferingHints<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints"></a>

The `ElasticsearchBufferingHints` property type specifies how Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) buffers incoming data while delivering it to the destination\. The first buffer condition that is satisfied triggers Kinesis Data Firehose to deliver the data\. 

ElasticsearchBufferingHints is the property type for the `BufferingHints` property of the [Amazon Kinesis Data Firehose DeliveryStream ElasticsearchDestinationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.html) property type\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-syntax.json"></a>

```
{
  "[IntervalInSeconds](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-intervalinseconds)" : Integer,
  "[SizeInMBs](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-sizeinmbs)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-syntax.yaml"></a>

```
  [IntervalInSeconds](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-intervalinseconds): Integer
  [SizeInMBs](#cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-sizeinmbs): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints-properties"></a>

`IntervalInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-intervalinseconds"></a>
The length of time, in seconds, that Kinesis Data Firehose buffers incoming data before delivering it to the destination\. For valid values, see the `IntervalInSeconds` content for the [BufferingHints](https://docs.aws.amazon.com/firehose/latest/APIReference/API_BufferingHints.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `60`  
*Maximum*: `900`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeInMBs`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchbufferinghints-sizeinmbs"></a>
The size of the buffer, in MBs, that Kinesis Data Firehose uses for incoming data before delivering it to the destination\. For valid values, see the `SizeInMBs` content for the [BufferingHints](https://docs.aws.amazon.com/firehose/latest/APIReference/API_BufferingHints.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)