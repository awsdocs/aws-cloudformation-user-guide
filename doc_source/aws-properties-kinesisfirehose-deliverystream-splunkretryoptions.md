# AWS::KinesisFirehose::DeliveryStream SplunkRetryOptions<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions"></a>

The `SplunkRetryOptions` property type specifies retry behavior in case Kinesis Data Firehose is unable to deliver documents to Splunk or if it doesn't receive an acknowledgment from Splunk

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions-syntax.json"></a>

```
{
  "[DurationInSeconds](#cfn-kinesisfirehose-deliverystream-splunkretryoptions-durationinseconds)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions-syntax.yaml"></a>

```
  [DurationInSeconds](#cfn-kinesisfirehose-deliverystream-splunkretryoptions-durationinseconds): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions-properties"></a>

`DurationInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-splunkretryoptions-durationinseconds"></a>
The total amount of time that Kinesis Data Firehose spends on retries\. This duration starts after the initial attempt to send data to Splunk fails\. It doesn't include the periods during which Kinesis Data Firehose waits for acknowledgment from Splunk after each attempt\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `7200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions--seealso"></a>
+  [SplunkRetryOptions](https://docs.aws.amazon.com/firehose/latest/APIReference/API_SplunkRetryOptions.html) in the *Amazon Kinesis Data Firehose API Reference*\. 

