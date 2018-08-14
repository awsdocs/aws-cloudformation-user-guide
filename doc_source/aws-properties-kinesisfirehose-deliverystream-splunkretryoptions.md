# Amazon Kinesis Data Firehose DeliveryStream SplunkRetryOptions<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions"></a>

<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions-description"></a>The `SplunkRetryOptions` property type specifies retry behavior in case Kinesis Data Firehose is unable to deliver documents to Splunk or if it doesn't receive an acknowledgment from Splunk\.

<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions-inheritance"></a> `SplunkRetryOptions` is a property of the [Amazon Kinesis Data Firehose DeliveryStream SplunkDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration.md) property type\.

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
The total amount of time that Kinesis Data Firehose spends on retries\. This duration starts after the initial attempt to send data to Splunk fails and doesn't include the periods during which Kinesis Data Firehose waits for acknowledgment from Splunk after each attempt\.  
Valid Range: Minimum value of 0\. Maximum value of 7200\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-kinesisfirehose-deliverystream-splunkretryoptions-seealso"></a>
+ [SplunkRetryOptions](http://docs.aws.amazon.com/firehose/latest/APIReference/API_SplunkRetryOptions.html) in the *Amazon Kinesis Data Firehose API Reference*