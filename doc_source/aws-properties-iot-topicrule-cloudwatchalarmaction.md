# AWS IoT TopicRule CloudwatchAlarmAction<a name="aws-properties-iot-topicrule-cloudwatchalarmaction"></a>

`CloudwatchAlarm` is a property of the `Actions` property that describes an action that updates a CloudWatch alarm\.

## Syntax<a name="w3ab2c21c14e1125b5"></a>

### JSON<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-alarmname)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-rolearn)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-statereason)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-statevalue)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-alarmname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-rolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-statereason): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchalarmaction-statevalue): String
```

## Properties<a name="w3ab2c21c14e1125b7"></a>

`AlarmName`  
The CloudWatch alarm name\.  
*Required: *Yes  
*Type*: String

`RoleArn`  
The IAM role that allows access to the CloudWatch alarm\.  
*Required: *Yes  
*Type*: String

`StateReason`  
The reason for the change of the alarm state\.  
*Required: *Yes  
*Type*: String

`StateValue`  
The value of the alarm state\.  
*Required: *Yes  
*Type*: String