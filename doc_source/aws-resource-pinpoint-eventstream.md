# AWS::Pinpoint::EventStream<a name="aws-resource-pinpoint-eventstream"></a>

You can configure Amazon Pinpoint to stream events to Amazon Kinesis Data Firehose or Amazon Kinesis Data Streams\. By streaming events, you enable more flexible options for analysis and storage\. The AWS::Pinpoint::EventStream resource defines the settings of an event stream for an Amazon Pinpoint application\.

You can configure only one event stream for each Amazon Pinpoint application\. To combine data from multiple applications, configure each application to use the same stream\.

## Syntax<a name="aws-resource-pinpoint-eventstream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-eventstream-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::EventStream",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-eventstream-applicationid)" : String,
      "[DestinationStreamArn](#cfn-pinpoint-eventstream-destinationstreamarn)" : String,
      "[RoleArn](#cfn-pinpoint-eventstream-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-eventstream-syntax.yaml"></a>

```
Type: AWS::Pinpoint::EventStream
Properties: 
  [ApplicationId](#cfn-pinpoint-eventstream-applicationid): String
  [DestinationStreamArn](#cfn-pinpoint-eventstream-destinationstreamarn): String
  [RoleArn](#cfn-pinpoint-eventstream-rolearn): String
```

## Properties<a name="aws-resource-pinpoint-eventstream-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-eventstream-applicationid"></a>
The unique identifier for the Amazon Pinpoint application that you want to publish event data for\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationStreamArn`  <a name="cfn-pinpoint-eventstream-destinationstreamarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Kinesis data stream or Amazon Kinesis Data Firehose delivery stream that you want to publish event data to\.  
For a Kinesis data stream, the ARN format is: `arn:aws:kinesis:region:account-id:stream/stream_name `   
For a Kinesis Data Firehose delivery stream, the ARN format is: `arn:aws:firehose:region:account-id:deliverystream/stream_name `   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-pinpoint-eventstream-rolearn"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that authorizes Amazon Pinpoint to publish event data to the stream in your AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-eventstream-return-values"></a>

### Ref<a name="aws-resource-pinpoint-eventstream-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the event stream is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.