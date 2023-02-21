# AWS::IoTEvents::AlarmModel AlarmCapabilities<a name="aws-properties-iotevents-alarmmodel-alarmcapabilities"></a>

Contains the configuration information of alarm state changes\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-alarmcapabilities-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-alarmcapabilities-syntax.json"></a>

```
{
  "[AcknowledgeFlow](#cfn-iotevents-alarmmodel-alarmcapabilities-acknowledgeflow)" : AcknowledgeFlow,
  "[InitializationConfiguration](#cfn-iotevents-alarmmodel-alarmcapabilities-initializationconfiguration)" : InitializationConfiguration
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-alarmcapabilities-syntax.yaml"></a>

```
  [AcknowledgeFlow](#cfn-iotevents-alarmmodel-alarmcapabilities-acknowledgeflow): 
    AcknowledgeFlow
  [InitializationConfiguration](#cfn-iotevents-alarmmodel-alarmcapabilities-initializationconfiguration): 
    InitializationConfiguration
```

## Properties<a name="aws-properties-iotevents-alarmmodel-alarmcapabilities-properties"></a>

`AcknowledgeFlow`  <a name="cfn-iotevents-alarmmodel-alarmcapabilities-acknowledgeflow"></a>
Specifies whether to get notified for alarm state changes\.  
*Required*: No  
*Type*: [AcknowledgeFlow](aws-properties-iotevents-alarmmodel-acknowledgeflow.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InitializationConfiguration`  <a name="cfn-iotevents-alarmmodel-alarmcapabilities-initializationconfiguration"></a>
Specifies the default alarm state\. The configuration applies to all alarms that were created based on this alarm model\.  
*Required*: No  
*Type*: [InitializationConfiguration](aws-properties-iotevents-alarmmodel-initializationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)