# AWS::IoT::TopicRule RepublishAction<a name="aws-properties-iot-topicrule-republishaction"></a>

Describes an action to republish to another topic\.

## Syntax<a name="aws-properties-iot-topicrule-republishaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-republishaction-syntax.json"></a>

```
{
  "[Qos](#cfn-iot-topicrule-republishaction-qos)" : Integer,
  "[RoleArn](#cfn-iot-topicrule-republishaction-rolearn)" : String,
  "[Topic](#cfn-iot-topicrule-republishaction-topic)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-republishaction-syntax.yaml"></a>

```
  [Qos](#cfn-iot-topicrule-republishaction-qos): Integer
  [RoleArn](#cfn-iot-topicrule-republishaction-rolearn): String
  [Topic](#cfn-iot-topicrule-republishaction-topic): String
```

## Properties<a name="aws-properties-iot-topicrule-republishaction-properties"></a>

`Qos`  <a name="cfn-iot-topicrule-republishaction-qos"></a>
The Quality of Service \(QoS\) level to use when republishing messages\. The default value is 0\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-republishaction-rolearn"></a>
The ARN of the IAM role that grants access\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Topic`  <a name="cfn-iot-topicrule-republishaction-topic"></a>
The name of the MQTT topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)