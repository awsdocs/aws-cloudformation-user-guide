# AWS::IoT::TopicRule IotEventsAction<a name="aws-properties-iot-topicrule-ioteventsaction"></a>

Sends an input to an AWS IoT Events detector\.

## Syntax<a name="aws-properties-iot-topicrule-ioteventsaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-ioteventsaction-syntax.json"></a>

```
{
  "[InputName](#cfn-iot-topicrule-ioteventsaction-inputname)" : String,
  "[MessageId](#cfn-iot-topicrule-ioteventsaction-messageid)" : String,
  "[RoleArn](#cfn-iot-topicrule-ioteventsaction-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-ioteventsaction-syntax.yaml"></a>

```
  [InputName](#cfn-iot-topicrule-ioteventsaction-inputname): String
  [MessageId](#cfn-iot-topicrule-ioteventsaction-messageid): String
  [RoleArn](#cfn-iot-topicrule-ioteventsaction-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-ioteventsaction-properties"></a>

`InputName`  <a name="cfn-iot-topicrule-ioteventsaction-inputname"></a>
The name of the AWS IoT Events input\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageId`  <a name="cfn-iot-topicrule-ioteventsaction-messageid"></a>
The ID of the message\. The default `messageId` is a new UUID value\.  
When `batchMode` is `true`, you can't specify a `messageId`\-\-a new UUID value will be assigned\.  
Assign a value to this property to ensure that only one input \(message\) with a given `messageId` will be processed by an AWS IoT Events detector\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-ioteventsaction-rolearn"></a>
The ARN of the role that grants AWS IoT permission to send an input to an AWS IoT Events detector\. \("Action":"iotevents:BatchPutMessage"\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)