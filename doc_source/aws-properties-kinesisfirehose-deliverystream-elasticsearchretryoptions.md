# AWS::KinesisFirehose::DeliveryStream ElasticsearchRetryOptions<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions"></a>

The `ElasticsearchRetryOptions` property type configures the retry behavior for when Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) can't deliver data to Amazon Elasticsearch Service \(Amazon ES\)\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
After an initial failure to deliver to Amazon ES, the total amount of time during which Kinesis Data Firehose re\-attempts delivery \(including the first attempt\)\. If Kinesis Data Firehose can't deliver the data within the specified time, it writes the data to the backup S3 bucket\. For valid values, see the `DurationInSeconds` content for the [ElasticsearchRetryOptions](https://docs.aws.amazon.com/firehose/latest/APIReference/API_ElasticsearchRetryOptions.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `7200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)