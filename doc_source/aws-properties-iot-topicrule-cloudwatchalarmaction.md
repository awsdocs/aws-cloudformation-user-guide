# AWS::IoT::TopicRule CloudwatchAlarmAction<a name="aws-properties-iot-topicrule-cloudwatchalarmaction"></a>

Describes an action that updates a CloudWatch alarm\.

## Syntax<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-syntax.json"></a>

```
{
  "[AlarmName](#cfn-iot-topicrule-cloudwatchalarmaction-alarmname)" : String,
  "[RoleArn](#cfn-iot-topicrule-cloudwatchalarmaction-rolearn)" : String,
  "[StateReason](#cfn-iot-topicrule-cloudwatchalarmaction-statereason)" : String,
  "[StateValue](#cfn-iot-topicrule-cloudwatchalarmaction-statevalue)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-syntax.yaml"></a>

```
  [AlarmName](#cfn-iot-topicrule-cloudwatchalarmaction-alarmname): String
  [RoleArn](#cfn-iot-topicrule-cloudwatchalarmaction-rolearn): String
  [StateReason](#cfn-iot-topicrule-cloudwatchalarmaction-statereason): String
  [StateValue](#cfn-iot-topicrule-cloudwatchalarmaction-statevalue): String
```

## Properties<a name="aws-properties-iot-topicrule-cloudwatchalarmaction-properties"></a>

`AlarmName`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-alarmname"></a>
The CloudWatch alarm name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-rolearn"></a>
The IAM role that allows access to the CloudWatch alarm\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StateReason`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-statereason"></a>
The reason for the alarm change\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StateValue`  <a name="cfn-iot-topicrule-cloudwatchalarmaction-statevalue"></a>
The value of the alarm state\. Acceptable values are: OK, ALARM, INSUFFICIENT\_DATA\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)