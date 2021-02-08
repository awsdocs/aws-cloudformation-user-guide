# AWS::IoTEvents::DetectorModel IotTopicPublish<a name="aws-properties-iotevents-detectormodel-iottopicpublish"></a>

Information required to publish the MQTT message through the AWS IoT message broker\.

## Syntax<a name="aws-properties-iotevents-detectormodel-iottopicpublish-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-iottopicpublish-syntax.json"></a>

```
{
  "[MqttTopic](#cfn-iotevents-detectormodel-iottopicpublish-mqtttopic)" : String,
  "[Payload](#cfn-iotevents-detectormodel-iottopicpublish-payload)" : Payload
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-iottopicpublish-syntax.yaml"></a>

```
  [MqttTopic](#cfn-iotevents-detectormodel-iottopicpublish-mqtttopic): String
  [Payload](#cfn-iotevents-detectormodel-iottopicpublish-payload): 
    Payload
```

## Properties<a name="aws-properties-iotevents-detectormodel-iottopicpublish-properties"></a>

`MqttTopic`  <a name="cfn-iotevents-detectormodel-iottopicpublish-mqtttopic"></a>
The MQTT topic of the message\. You can use a string expression that includes variables \(`$variable.<variable-name>`\) and input values \(`$input.<input-name>.<path-to-datum>`\) as the topic string\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Payload`  <a name="cfn-iotevents-detectormodel-iottopicpublish-payload"></a>
You can configure the action payload when you publish a message to an AWS IoT Core topic\.  
*Required*: No  
*Type*: [Payload](aws-properties-iotevents-detectormodel-payload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)