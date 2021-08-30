# AWS::CloudFront::RealtimeLogConfig EndPoint<a name="aws-properties-cloudfront-realtimelogconfig-endpoint"></a>

Contains information about the Amazon Kinesis data stream where you are sending real\-time log data in a real\-time log configuration\.

## Syntax<a name="aws-properties-cloudfront-realtimelogconfig-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-realtimelogconfig-endpoint-syntax.json"></a>

```
{
  "[KinesisStreamConfig](#cfn-cloudfront-realtimelogconfig-endpoint-kinesisstreamconfig)" : KinesisStreamConfig,
  "[StreamType](#cfn-cloudfront-realtimelogconfig-endpoint-streamtype)" : String
}
```

### YAML<a name="aws-properties-cloudfront-realtimelogconfig-endpoint-syntax.yaml"></a>

```
  [KinesisStreamConfig](#cfn-cloudfront-realtimelogconfig-endpoint-kinesisstreamconfig): 
    KinesisStreamConfig
  [StreamType](#cfn-cloudfront-realtimelogconfig-endpoint-streamtype): String
```

## Properties<a name="aws-properties-cloudfront-realtimelogconfig-endpoint-properties"></a>

`KinesisStreamConfig`  <a name="cfn-cloudfront-realtimelogconfig-endpoint-kinesisstreamconfig"></a>
Contains information about the Amazon Kinesis data stream where you are sending real\-time log data\.  
*Required*: Yes  
*Type*: [KinesisStreamConfig](aws-properties-cloudfront-realtimelogconfig-kinesisstreamconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamType`  <a name="cfn-cloudfront-realtimelogconfig-endpoint-streamtype"></a>
The type of data stream where you are sending real\-time log data\. The only valid value is `Kinesis`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)