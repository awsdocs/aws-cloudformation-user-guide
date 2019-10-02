# AWS::IoTEvents::DetectorModel IotTopicPublish<a name="aws-properties-iotevents-detectormodel-iottopicpublish"></a>

Sends information about the detector model instance and the event which triggered the action in an MQTT message with the given topic to the AWS IoT message broker\.

## Syntax<a name="aws-properties-iotevents-detectormodel-iottopicpublish-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-iottopicpublish-syntax.json"></a>

```
{
  "[MqttTopic](#cfn-iotevents-detectormodel-iottopicpublish-mqtttopic)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-iottopicpublish-syntax.yaml"></a>

```
  [MqttTopic](#cfn-iotevents-detectormodel-iottopicpublish-mqtttopic): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-iottopicpublish-properties"></a>

`MqttTopic`  <a name="cfn-iotevents-detectormodel-iottopicpublish-mqtttopic"></a>
The MQTT topic of the message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
