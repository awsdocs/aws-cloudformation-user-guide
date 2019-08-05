# AWS::IoTEvents::DetectorModel IotEvents<a name="aws-properties-iotevents-detectormodel-iotevents"></a>

Sends an IoT Events input, passing in information about the detector model instance and the event which triggered the action\.

## Syntax<a name="aws-properties-iotevents-detectormodel-iotevents-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-iotevents-syntax.json"></a>

```
{
  "[InputName](#cfn-iotevents-detectormodel-iotevents-inputname)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-iotevents-syntax.yaml"></a>

```
  [InputName](#cfn-iotevents-detectormodel-iotevents-inputname): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-iotevents-properties"></a>

`InputName`  <a name="cfn-iotevents-detectormodel-iotevents-inputname"></a>
The name of the AWS IoT Events input where the data is sent\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
