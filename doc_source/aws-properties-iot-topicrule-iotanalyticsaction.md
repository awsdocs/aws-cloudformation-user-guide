# AWS IoT TopicRule IotAnalyticsAction<a name="aws-properties-iot-topicrule-iotanalyticsaction"></a>

<a name="aws-properties-iot-topicrule-iotanalyticsaction-description"></a>The `IotAnalyticsAction` property type sends messge data to an AWS IoT Analytics channel\.

<a name="aws-properties-iot-topicrule-iotanalyticsaction-inheritance"></a> `IotAnalyticsAction` is a property of the [Action](aws-properties-iot-topicrule-action.md) property type\.

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
The name of the AWS IoT Analytics channel to which message data will be sent\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-iot-topicrule-iotanalyticsaction-rolearn"></a>
The ARN of the role which has a policy that grants AWS IoT Analytics permission to send message data via AWS IoT Analytics \(iotanalytics:BatchPutMessage\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iot-topicrule-iotanalyticsaction-seealso"></a>
+ [IotAnalyticsAction](https://docs.aws.amazon.com/iot/latest/apireference/API_IotAnalyticsAction.html) in the *AWS IoT API Reference*