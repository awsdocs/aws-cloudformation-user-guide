# AWS::IoT::TopicRule IotAnalyticsAction<a name="aws-properties-iot-topicrule-iotanalyticsaction"></a>

Sends message data to an AWS IoT Analytics channel\.

## Syntax<a name="aws-properties-iot-topicrule-iotanalyticsaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-iotanalyticsaction-syntax.json"></a>

```
{
  "[ChannelName](#cfn-iot-topicrule-iotanalyticsaction-channelname)" : String,
  "[RoleArn](#cfn-iot-topicrule-iotanalyticsaction-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-iotanalyticsaction-syntax.yaml"></a>

```
  [ChannelName](#cfn-iot-topicrule-iotanalyticsaction-channelname): String
  [RoleArn](#cfn-iot-topicrule-iotanalyticsaction-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-iotanalyticsaction-properties"></a>

`ChannelName`  <a name="cfn-iot-topicrule-iotanalyticsaction-channelname"></a>
The name of the IoT Analytics channel to which message data will be sent\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-iotanalyticsaction-rolearn"></a>
The ARN of the role which has a policy that grants IoT Analytics permission to send message data via IoT Analytics \(iotanalytics:BatchPutMessage\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-iot-topicrule-iotanalyticsaction--seealso"></a>
+  [IotAnalyticsAction](https://docs.aws.amazon.com/iot/latest/apireference/API_IotAnalyticsAction.html) in the *AWS IoT API Reference*\.

