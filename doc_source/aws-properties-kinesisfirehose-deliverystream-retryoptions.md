# AWS::KinesisFirehose::DeliveryStream RetryOptions<a name="aws-properties-kinesisfirehose-deliverystream-retryoptions"></a>

Describes the retry behavior in case Kinesis Data Firehose is unable to deliver data to the specified HTTP endpoint destination, or if it doesn't receive a valid acknowledgment of receipt from the specified HTTP endpoint destination\. Kinesis Firehose supports any custom HTTP endpoint or HTTP endpoints owned by supported third\-party service providers, including Datadog, MongoDB, and New Relic\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-retryoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-retryoptions-syntax.json"></a>

```
{
  "[DurationInSeconds](#cfn-kinesisfirehose-deliverystream-retryoptions-durationinseconds)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-retryoptions-syntax.yaml"></a>

```
  [DurationInSeconds](#cfn-kinesisfirehose-deliverystream-retryoptions-durationinseconds): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-retryoptions-properties"></a>

`DurationInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-retryoptions-durationinseconds"></a>
The total amount of time that Kinesis Data Firehose spends on retries\. This duration starts after the initial attempt to send data to the custom destination via HTTPS endpoint fails\. It doesn't include the periods during which Kinesis Data Firehose waits for acknowledgment from the specified destination after each attempt\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `7200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)