# AWS::IoTEvents::AlarmModel Sns<a name="aws-properties-iotevents-alarmmodel-sns"></a>

Information required to publish the Amazon SNS message\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-sns-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-sns-syntax.json"></a>

```
{
  "[Payload](#cfn-iotevents-alarmmodel-sns-payload)" : Payload,
  "[TargetArn](#cfn-iotevents-alarmmodel-sns-targetarn)" : String
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-sns-syntax.yaml"></a>

```
  [Payload](#cfn-iotevents-alarmmodel-sns-payload): 
    Payload
  [TargetArn](#cfn-iotevents-alarmmodel-sns-targetarn): String
```

## Properties<a name="aws-properties-iotevents-alarmmodel-sns-properties"></a>

`Payload`  <a name="cfn-iotevents-alarmmodel-sns-payload"></a>
You can configure the action payload when you send a message as an Amazon SNS push notification\.  
*Required*: No  
*Type*: [Payload](aws-properties-iotevents-alarmmodel-payload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-iotevents-alarmmodel-sns-targetarn"></a>
The ARN of the Amazon SNS target where the message is sent\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)