# AWS::IoT::TopicRule Timestamp<a name="aws-properties-iot-topicrule-timestamp"></a>

Describes how to interpret an application\-defined timestamp value from an MQTT message payload and the precision of that value\.

## Syntax<a name="aws-properties-iot-topicrule-timestamp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-timestamp-syntax.json"></a>

```
{
  "[Unit](#cfn-iot-topicrule-timestamp-unit)" : String,
  "[Value](#cfn-iot-topicrule-timestamp-value)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-timestamp-syntax.yaml"></a>

```
  [Unit](#cfn-iot-topicrule-timestamp-unit): String
  [Value](#cfn-iot-topicrule-timestamp-value): String
```

## Properties<a name="aws-properties-iot-topicrule-timestamp-properties"></a>

`Unit`  <a name="cfn-iot-topicrule-timestamp-unit"></a>
The precision of the timestamp value that results from the expression described in `value`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iot-topicrule-timestamp-value"></a>
An expression that returns a long epoch time value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)