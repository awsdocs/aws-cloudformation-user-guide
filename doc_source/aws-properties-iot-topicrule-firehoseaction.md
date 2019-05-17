# AWS::IoT::TopicRule FirehoseAction<a name="aws-properties-iot-topicrule-firehoseaction"></a>

Describes an action that writes data to an Amazon Kinesis Firehose stream\.

## Syntax<a name="aws-properties-iot-topicrule-firehoseaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-firehoseaction-syntax.json"></a>

```
{
  "[DeliveryStreamName](#cfn-iot-topicrule-firehoseaction-deliverystreamname)" : String,
  "[RoleArn](#cfn-iot-topicrule-firehoseaction-rolearn)" : String,
  "[Separator](#cfn-iot-topicrule-firehoseaction-separator)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-firehoseaction-syntax.yaml"></a>

```
  [DeliveryStreamName](#cfn-iot-topicrule-firehoseaction-deliverystreamname): String
  [RoleArn](#cfn-iot-topicrule-firehoseaction-rolearn): String
  [Separator](#cfn-iot-topicrule-firehoseaction-separator): String
```

## Properties<a name="aws-properties-iot-topicrule-firehoseaction-properties"></a>

`DeliveryStreamName`  <a name="cfn-iot-topicrule-firehoseaction-deliverystreamname"></a>
The delivery stream name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-firehoseaction-rolearn"></a>
The IAM role that grants access to the Amazon Kinesis Firehose stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Separator`  <a name="cfn-iot-topicrule-firehoseaction-separator"></a>
A character separator that will be used to separate records written to the Firehose stream\. Valid values are: '\\n' \(newline\), '\\t' \(tab\), '\\r\\n' \(Windows newline\), ',' \(comma\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)