# AWS::IoTEvents::AlarmModel AlarmRule<a name="aws-properties-iotevents-alarmmodel-alarmrule"></a>

Defines when your alarm is invoked\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-alarmrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-alarmrule-syntax.json"></a>

```
{
  "[SimpleRule](#cfn-iotevents-alarmmodel-alarmrule-simplerule)" : SimpleRule
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-alarmrule-syntax.yaml"></a>

```
  [SimpleRule](#cfn-iotevents-alarmmodel-alarmrule-simplerule): 
    SimpleRule
```

## Properties<a name="aws-properties-iotevents-alarmmodel-alarmrule-properties"></a>

`SimpleRule`  <a name="cfn-iotevents-alarmmodel-alarmrule-simplerule"></a>
A rule that compares an input property value to a threshold value with a comparison operator\.  
*Required*: No  
*Type*: [SimpleRule](aws-properties-iotevents-alarmmodel-simplerule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)