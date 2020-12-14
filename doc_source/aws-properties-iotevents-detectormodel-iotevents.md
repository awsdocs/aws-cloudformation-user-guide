# AWS::IoTEvents::DetectorModel IotEvents<a name="aws-properties-iotevents-detectormodel-iotevents"></a>

Sends an AWS IoT Events input, passing in information about the detector model instance and the event that triggered the action\.

## Syntax<a name="aws-properties-iotevents-detectormodel-iotevents-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-iotevents-syntax.json"></a>

```
{
  "[InputName](#cfn-iotevents-detectormodel-iotevents-inputname)" : String,
  "[Payload](#cfn-iotevents-detectormodel-iotevents-payload)" : Payload
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-iotevents-syntax.yaml"></a>

```
  [InputName](#cfn-iotevents-detectormodel-iotevents-inputname): String
  [Payload](#cfn-iotevents-detectormodel-iotevents-payload): 
    Payload
```

## Properties<a name="aws-properties-iotevents-detectormodel-iotevents-properties"></a>

`InputName`  <a name="cfn-iotevents-detectormodel-iotevents-inputname"></a>
The name of the AWS IoT Events input where the data is sent\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Payload`  <a name="cfn-iotevents-detectormodel-iotevents-payload"></a>
You can configure the action payload when you send a message to an AWS IoT Events input\.  
*Required*: No  
*Type*: [Payload](aws-properties-iotevents-detectormodel-payload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)