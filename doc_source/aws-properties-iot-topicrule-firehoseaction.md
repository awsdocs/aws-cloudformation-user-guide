# AWS IoT TopicRule FirehoseAction<a name="aws-properties-iot-topicrule-firehoseaction"></a>

`Firehose` is a property of the `Actions` property that describes an action that writes data to a Kinesis Data Firehose stream\.

## Syntax<a name="w3ab2c21c14e1346b5"></a>

### JSON<a name="aws-properties-iot-topicrule-firehoseaction-syntax.json"></a>

```
{
  "[DeliveryStreamName](#cfn-iot-topicrule-firehoseaction-deliverystreamname)": String,
  "[RoleArn](#cfn-iot-topicrule-firehoseaction-rolearn)": String,
  "[Separator](#cfn-iot-topicrule-firehoseaction-separator)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-firehoseaction-syntax.yaml"></a>

```
[DeliveryStreamName](#cfn-iot-topicrule-firehoseaction-deliverystreamname): String
[RoleArn](#cfn-iot-topicrule-firehoseaction-rolearn): String
[Separator](#cfn-iot-topicrule-firehoseaction-separator): String
```

## Properties<a name="w3ab2c21c14e1346b7"></a>

`DeliveryStreamName`  <a name="cfn-iot-topicrule-firehoseaction-deliverystreamname"></a>
The delivery stream name\.  
*Required*: Yes  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-firehoseaction-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that grants access to the Kinesis Data Firehose stream\.  
*Required*: Yes  
*Type*: String

`Separator`  <a name="cfn-iot-topicrule-firehoseaction-separator"></a>
A character separator that's used to separate records written to the Kinesis Data Firehose stream\. For valid values, see [Firehose Action](http://docs.aws.amazon.com/iot/latest/developerguide/firehose-rule.html) in the *AWS IoT Developer Guide*\.  
*Required*: No  
*Type*: String