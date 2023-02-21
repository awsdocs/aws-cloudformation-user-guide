# AWS::IoTEvents::AlarmModel AcknowledgeFlow<a name="aws-properties-iotevents-alarmmodel-acknowledgeflow"></a>

Specifies whether to get notified for alarm state changes\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-acknowledgeflow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-acknowledgeflow-syntax.json"></a>

```
{
  "[Enabled](#cfn-iotevents-alarmmodel-acknowledgeflow-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-acknowledgeflow-syntax.yaml"></a>

```
  [Enabled](#cfn-iotevents-alarmmodel-acknowledgeflow-enabled): Boolean
```

## Properties<a name="aws-properties-iotevents-alarmmodel-acknowledgeflow-properties"></a>

`Enabled`  <a name="cfn-iotevents-alarmmodel-acknowledgeflow-enabled"></a>
The value must be `TRUE` or `FALSE`\. If `TRUE`, you receive a notification when the alarm state changes\. You must choose to acknowledge the notification before the alarm state can return to `NORMAL`\. If `FALSE`, you won't receive notifications\. The alarm automatically changes to the `NORMAL` state when the input property value returns to the specified range\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)