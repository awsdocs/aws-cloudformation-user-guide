# Amazon Kinesis Firehose DeliveryStream ElasticsearchRetryOptions<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions"></a>

The `ElasticsearchRetryOptions` property type configures the retry behavior for when Amazon Kinesis Firehose \(Kinesis Firehose\) can't deliver data to Amazon Elasticsearch Service \(Amazon ES\)\.

`RetryOptions` is a property of the [Amazon Kinesis Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md) property type\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions-syntax.json"></a>

```
{
  "[DurationInSeconds](#cfn-kinesisfirehose-deliverystream-elasticsearchretryoptions-durationinseconds)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions-syntax.yaml"></a>

```
[DurationInSeconds](#cfn-kinesisfirehose-deliverystream-elasticsearchretryoptions-durationinseconds): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions-properties"></a>

`DurationInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchretryoptions-durationinseconds"></a>
After an initial failure to deliver to Amazon ES, the total amount of time during which Kinesis Firehose re\-attempts delivery \(including the first attempt\)\. If Kinesis Firehose can't deliver the data within the specified time, it writes the data to the backup S3 bucket\. For valid values, see the `DurationInSeconds` content for the [ElasticsearchRetryOptions](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ElasticsearchRetryOptions.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required*: Yes  
*Type*: Integer