# AWS::KafkaConnect::Connector CloudWatchLogsLogDelivery<a name="aws-properties-kafkaconnect-connector-cloudwatchlogslogdelivery"></a>

The settings for delivering connector logs to Amazon CloudWatch Logs\.

## Syntax<a name="aws-properties-kafkaconnect-connector-cloudwatchlogslogdelivery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-cloudwatchlogslogdelivery-syntax.json"></a>

```
{
  "[Enabled](#cfn-kafkaconnect-connector-cloudwatchlogslogdelivery-enabled)" : Boolean,
  "[LogGroup](#cfn-kafkaconnect-connector-cloudwatchlogslogdelivery-loggroup)" : String
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-cloudwatchlogslogdelivery-syntax.yaml"></a>

```
  [Enabled](#cfn-kafkaconnect-connector-cloudwatchlogslogdelivery-enabled): Boolean
  [LogGroup](#cfn-kafkaconnect-connector-cloudwatchlogslogdelivery-loggroup): String
```

## Properties<a name="aws-properties-kafkaconnect-connector-cloudwatchlogslogdelivery-properties"></a>

`Enabled`  <a name="cfn-kafkaconnect-connector-cloudwatchlogslogdelivery-enabled"></a>
Whether log delivery to Amazon CloudWatch Logs is enabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogGroup`  <a name="cfn-kafkaconnect-connector-cloudwatchlogslogdelivery-loggroup"></a>
The name of the CloudWatch log group that is the destination for log delivery\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)