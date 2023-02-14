# AWS::IoT::TopicRule TimestreamTimestamp<a name="aws-properties-iot-topicrule-timestreamtimestamp"></a>

The value to use for the entry's timestamp\. If blank, the time that the entry was processed is used\.

## Syntax<a name="aws-properties-iot-topicrule-timestreamtimestamp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-timestreamtimestamp-syntax.json"></a>

```
{
  "[Unit](#cfn-iot-topicrule-timestreamtimestamp-unit)" : String,
  "[Value](#cfn-iot-topicrule-timestreamtimestamp-value)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-timestreamtimestamp-syntax.yaml"></a>

```
  [Unit](#cfn-iot-topicrule-timestreamtimestamp-unit): String
  [Value](#cfn-iot-topicrule-timestreamtimestamp-value): String
```

## Properties<a name="aws-properties-iot-topicrule-timestreamtimestamp-properties"></a>

`Unit`  <a name="cfn-iot-topicrule-timestreamtimestamp-unit"></a>
The precision of the timestamp value that results from the expression described in `value`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iot-topicrule-timestreamtimestamp-value"></a>
An expression that returns a long epoch time value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)