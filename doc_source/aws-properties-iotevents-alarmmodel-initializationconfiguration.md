# AWS::IoTEvents::AlarmModel InitializationConfiguration<a name="aws-properties-iotevents-alarmmodel-initializationconfiguration"></a>

Specifies the default alarm state\. The configuration applies to all alarms that were created based on this alarm model\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-initializationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-initializationconfiguration-syntax.json"></a>

```
{
  "[DisabledOnInitialization](#cfn-iotevents-alarmmodel-initializationconfiguration-disabledoninitialization)" : Boolean
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-initializationconfiguration-syntax.yaml"></a>

```
  [DisabledOnInitialization](#cfn-iotevents-alarmmodel-initializationconfiguration-disabledoninitialization): Boolean
```

## Properties<a name="aws-properties-iotevents-alarmmodel-initializationconfiguration-properties"></a>

`DisabledOnInitialization`  <a name="cfn-iotevents-alarmmodel-initializationconfiguration-disabledoninitialization"></a>
The value must be `TRUE` or `FALSE`\. If `FALSE`, all alarm instances created based on the alarm model are activated\. The default value is `TRUE`\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)