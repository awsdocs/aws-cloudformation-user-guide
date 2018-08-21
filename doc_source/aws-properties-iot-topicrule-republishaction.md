# AWS IoT TopicRule RepublishAction<a name="aws-properties-iot-topicrule-republishaction"></a>

`Republish` is a property of the `Actions` property that describes an action that publishes data to an MQ Telemetry Transport \(MQTT\) topic different from the one currently specified\.

## Syntax<a name="w3ab2c21c14e1365b5"></a>

### JSON<a name="aws-properties-iot-topicrule-republishaction-syntax.json"></a>

```
{
  "[RoleArn](#cfn-iot-topicrule-republishaction-rolearn)": String,
  "[Topic](#cfn-iot-topicrule-republishaction-topic)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-republishaction-syntax.yaml"></a>

```
[RoleArn](#cfn-iot-topicrule-republishaction-rolearn): String
[Topic](#cfn-iot-topicrule-republishaction-topic): String
```

## Properties<a name="w3ab2c21c14e1365b7"></a>

`RoleArn`  <a name="cfn-iot-topicrule-republishaction-rolearn"></a>
The ARN of the IAM role that grants publishing access\.  
*Required*: Yes  
*Type*: String

`Topic`  <a name="cfn-iot-topicrule-republishaction-topic"></a>
The name of the MQTT topic topic different from the one currently specified\.  
*Required*: Yes  
*Type*: String