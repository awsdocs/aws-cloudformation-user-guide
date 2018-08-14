# AWS IoT TopicRule CloudwatchAlarmAction<a name="aws-properties-iot-topicrule-cloudwatchalarmaction"></a>

`CloudwatchAlarm` is a property of the `Actions` property that describes an action that updates a CloudWatch alarm\.

## Syntax<a name="w3ab2c21c14e1322b5"></a>

### JSON<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-syntax.json"></a>

```
{
  "[AlarmName](#cfn-iot-topicrule-cloudwatchalarmaction-alarmname)": String,
  "[RoleArn](#cfn-iot-topicrule-cloudwatchalarmaction-rolearn)": String,
  "[StateReason](#cfn-iot-topicrule-cloudwatchalarmaction-statereason)": String,
  "[StateValue](#cfn-iot-topicrule-cloudwatchalarmaction-statevalue)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-syntax.yaml"></a>

```
[AlarmName](#cfn-iot-topicrule-cloudwatchalarmaction-alarmname): String
[RoleArn](#cfn-iot-topicrule-cloudwatchalarmaction-rolearn): String
[StateReason](#cfn-iot-topicrule-cloudwatchalarmaction-statereason): String
[StateValue](#cfn-iot-topicrule-cloudwatchalarmaction-statevalue): String
```

## Properties<a name="w3ab2c21c14e1322b7"></a>

`AlarmName`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-alarmname"></a>
The CloudWatch alarm name\.  
*Required*: Yes  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-rolearn"></a>
The IAM role that allows access to the CloudWatch alarm\.  
*Required*: Yes  
*Type*: String

`StateReason`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-statereason"></a>
The reason for the change of the alarm state\.  
*Required*: Yes  
*Type*: String

`StateValue`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-statevalue"></a>
The value of the alarm state\.  
*Required*: Yes  
*Type*: String