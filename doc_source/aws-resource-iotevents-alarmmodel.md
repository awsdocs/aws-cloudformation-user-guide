# AWS::IoTEvents::AlarmModel<a name="aws-resource-iotevents-alarmmodel"></a>

Represents an alarm model to monitor an AWS IoT Events input attribute\. You can use the alarm to get notified when the value is outside a specified range\. For more information, see [Create an alarm model](https://docs.aws.amazon.com/iotevents/latest/developerguide/create-alarms.html) in the * AWS IoT Events Developer Guide*\.

## Syntax<a name="aws-resource-iotevents-alarmmodel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotevents-alarmmodel-syntax.json"></a>

```
{
  "Type" : "AWS::IoTEvents::AlarmModel",
  "Properties" : {
      "[AlarmCapabilities](#cfn-iotevents-alarmmodel-alarmcapabilities)" : AlarmCapabilities,
      "[AlarmEventActions](#cfn-iotevents-alarmmodel-alarmeventactions)" : AlarmEventActions,
      "[AlarmModelDescription](#cfn-iotevents-alarmmodel-alarmmodeldescription)" : String,
      "[AlarmModelName](#cfn-iotevents-alarmmodel-alarmmodelname)" : String,
      "[AlarmRule](#cfn-iotevents-alarmmodel-alarmrule)" : AlarmRule,
      "[Key](#cfn-iotevents-alarmmodel-key)" : String,
      "[RoleArn](#cfn-iotevents-alarmmodel-rolearn)" : String,
      "[Severity](#cfn-iotevents-alarmmodel-severity)" : Integer,
      "[Tags](#cfn-iotevents-alarmmodel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotevents-alarmmodel-syntax.yaml"></a>

```
Type: AWS::IoTEvents::AlarmModel
Properties: 
  [AlarmCapabilities](#cfn-iotevents-alarmmodel-alarmcapabilities): 
    AlarmCapabilities
  [AlarmEventActions](#cfn-iotevents-alarmmodel-alarmeventactions): 
    AlarmEventActions
  [AlarmModelDescription](#cfn-iotevents-alarmmodel-alarmmodeldescription): String
  [AlarmModelName](#cfn-iotevents-alarmmodel-alarmmodelname): String
  [AlarmRule](#cfn-iotevents-alarmmodel-alarmrule): 
    AlarmRule
  [Key](#cfn-iotevents-alarmmodel-key): String
  [RoleArn](#cfn-iotevents-alarmmodel-rolearn): String
  [Severity](#cfn-iotevents-alarmmodel-severity): Integer
  [Tags](#cfn-iotevents-alarmmodel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotevents-alarmmodel-properties"></a>

`AlarmCapabilities`  <a name="cfn-iotevents-alarmmodel-alarmcapabilities"></a>
Contains the configuration information of alarm state changes\.  
*Required*: No  
*Type*: [AlarmCapabilities](aws-properties-iotevents-alarmmodel-alarmcapabilities.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmEventActions`  <a name="cfn-iotevents-alarmmodel-alarmeventactions"></a>
Contains information about one or more alarm actions\.  
*Required*: No  
*Type*: [AlarmEventActions](aws-properties-iotevents-alarmmodel-alarmeventactions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmModelDescription`  <a name="cfn-iotevents-alarmmodel-alarmmodeldescription"></a>
The description of the alarm model\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmModelName`  <a name="cfn-iotevents-alarmmodel-alarmmodelname"></a>
The name of the alarm model\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AlarmRule`  <a name="cfn-iotevents-alarmmodel-alarmrule"></a>
Defines when your alarm is invoked\.  
*Required*: Yes  
*Type*: [AlarmRule](aws-properties-iotevents-alarmmodel-alarmrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-iotevents-alarmmodel-key"></a>
An input attribute used as a key to create an alarm\. AWS IoT Events routes [inputs](https://docs.aws.amazon.com/iotevents/latest/apireference/API_Input.html) associated with this key to the alarm\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^((`[\w\- ]+`)|([\w\-]+))(\.((`[\w- ]+`)|([\w\-]+)))*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-iotevents-alarmmodel-rolearn"></a>
The ARN of the IAM role that allows the alarm to perform actions and access AWS resources\. For more information, see [Amazon Resource Names \(ARNs\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the * AWS General Reference*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Severity`  <a name="cfn-iotevents-alarmmodel-severity"></a>
A non\-negative integer that reflects the severity level of the alarm\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotevents-alarmmodel-tags"></a>
A list of key\-value pairs that contain metadata for the alarm model\. The tags help you manage the alarm model\. For more information, see [Tagging your AWS IoT Events resources](https://docs.aws.amazon.com/iotevents/latest/developerguide/tagging-iotevents.html) in the * AWS IoT Events Developer Guide*\.  
You can create up to 50 tags for one alarm model\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotevents-alarmmodel-return-values"></a>

### Ref<a name="aws-resource-iotevents-alarmmodel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the alarm model\. For example:

`{"Ref": "myAlarmModel"}`

For the AWS IoT Events alarm model `myAlarmModel`, `Ref` returns the name of the alarm model\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.