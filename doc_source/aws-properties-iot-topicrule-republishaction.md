# AWS IoT TopicRule RepublishAction<a name="aws-properties-iot-topicrule-republishaction"></a>

`Republish` is a property of the `Actions` property that describes an action that publishes data to an MQ Telemetry Transport \(MQTT\) topic different from the one currently specified\.

## Syntax<a name="w3ab2c21c14e1168b5"></a>

### JSON<a name="aws-properties-iot-topicrule-republishaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-republishaction-rolearn)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-republishaction-topic)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-republishaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-republishaction-rolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-republishaction-topic): String
```

## Properties<a name="w3ab2c21c14e1168b7"></a>

`RoleArn`  
The ARN of the IAM role that grants publishing access\.  
*Required: *Yes  
*Type*: String

`Topic`  
The name of the MQTT topic topic different from the one currently specified\.  
*Required: *Yes  
*Type*: String