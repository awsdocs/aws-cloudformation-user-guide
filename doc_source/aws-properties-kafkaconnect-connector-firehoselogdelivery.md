# AWS::KafkaConnect::Connector FirehoseLogDelivery<a name="aws-properties-kafkaconnect-connector-firehoselogdelivery"></a>

The settings for delivering logs to Amazon Kinesis Data Firehose\.

## Syntax<a name="aws-properties-kafkaconnect-connector-firehoselogdelivery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-firehoselogdelivery-syntax.json"></a>

```
{
  "[DeliveryStream](#cfn-kafkaconnect-connector-firehoselogdelivery-deliverystream)" : String,
  "[Enabled](#cfn-kafkaconnect-connector-firehoselogdelivery-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-firehoselogdelivery-syntax.yaml"></a>

```
  [DeliveryStream](#cfn-kafkaconnect-connector-firehoselogdelivery-deliverystream): String
  [Enabled](#cfn-kafkaconnect-connector-firehoselogdelivery-enabled): Boolean
```

## Properties<a name="aws-properties-kafkaconnect-connector-firehoselogdelivery-properties"></a>

`DeliveryStream`  <a name="cfn-kafkaconnect-connector-firehoselogdelivery-deliverystream"></a>
The name of the Kinesis Data Firehose delivery stream that is the destination for log delivery\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-kafkaconnect-connector-firehoselogdelivery-enabled"></a>
Specifies whether connector logs get delivered to Amazon Kinesis Data Firehose\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)