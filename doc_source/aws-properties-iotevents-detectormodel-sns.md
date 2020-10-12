# AWS::IoTEvents::DetectorModel Sns<a name="aws-properties-iotevents-detectormodel-sns"></a>

Information required to publish the Amazon SNS message\.

## Syntax<a name="aws-properties-iotevents-detectormodel-sns-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-sns-syntax.json"></a>

```
{
  "[Payload](#cfn-iotevents-detectormodel-sns-payload)" : Payload,
  "[TargetArn](#cfn-iotevents-detectormodel-sns-targetarn)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-sns-syntax.yaml"></a>

```
  [Payload](#cfn-iotevents-detectormodel-sns-payload): 
    Payload
  [TargetArn](#cfn-iotevents-detectormodel-sns-targetarn): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-sns-properties"></a>

`Payload`  <a name="cfn-iotevents-detectormodel-sns-payload"></a>
You can configure the action payload when you send a message as an Amazon SNS push notification\.  
*Required*: No  
*Type*: [Payload](aws-properties-iotevents-detectormodel-payload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-iotevents-detectormodel-sns-targetarn"></a>
The ARN of the Amazon SNS target where the message is sent\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)