# AWS::IoT1Click::Device<a name="aws-resource-iot1click-device"></a>

The `AWS::IoT1Click::Device` resource controls the enabled state of an AWS IoT 1\-Click compatible device\. For more information, see [Device](https://docs.aws.amazon.com/iot-1-click/1.0/devices-apireference/devices-deviceid.html) in the *AWS IoT 1\-Click Devices API Reference*\.

## Syntax<a name="aws-resource-iot1click-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot1click-device-syntax.json"></a>

```
{
  "Type" : "AWS::IoT1Click::Device",
  "Properties" : {
      "[DeviceId](#cfn-iot1click-device-deviceid)" : String,
      "[Enabled](#cfn-iot1click-device-enabled)" : Boolean
    }
}
```

### YAML<a name="aws-resource-iot1click-device-syntax.yaml"></a>

```
Type: AWS::IoT1Click::Device
Properties: 
  [DeviceId](#cfn-iot1click-device-deviceid): String
  [Enabled](#cfn-iot1click-device-enabled): Boolean
```

## Properties<a name="aws-resource-iot1click-device-properties"></a>

`DeviceId`  <a name="cfn-iot1click-device-deviceid"></a>
The ID of the device, such as `G030PX0312744DWM`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-iot1click-device-enabled"></a>
A Boolean value indicating whether the device is enabled \(`true`\) or not \(`false`\)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot1click-device-return-values"></a>

### Ref<a name="aws-resource-iot1click-device-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the device ARN, such as `arn:aws:iot1click:us-west-2:123456789012:devices/G030PX0312744DWM`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot1click-device-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot1click-device-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the device, such as `arn:aws:iot1click:us-west-2:123456789012:devices/G030PX0312744DWM`\.

`DeviceId`  <a name="DeviceId-fn::getatt"></a>
The unique identifier of the device\.

`Enabled`  <a name="Enabled-fn::getatt"></a>
A Boolean value indicating whether the device is enabled \(`true`\) or not \(`false`\)\.

## Examples<a name="aws-resource-iot1click-device--examples"></a>

### Enable an AWS IoT Device<a name="aws-resource-iot1click-device--examples--Enable_an_AWS_IoT_Device"></a>

#### JSON<a name="aws-resource-iot1click-device--examples--Enable_an_AWS_IoT_Device--json"></a>

```
{
  "SampleDevice": {
    "Type": "AWS::IoT1Click::Device",
    "Properties": {
      "DeviceId": "G030PX0312744DWM",
      "Enabled": true
    }
  }
}
```

#### YAML<a name="aws-resource-iot1click-device--examples--Enable_an_AWS_IoT_Device--yaml"></a>

```
SampleDevice:
  Type: "AWS::IoT1Click::Device"
  Properties:
    DeviceId: G030PX0312744DWM
    Enabled: True
```

## See also<a name="aws-resource-iot1click-device--seealso"></a>
+ [Device](https://docs.aws.amazon.com/iot-1-click/1.0/devices-apireference/devices-deviceid.html)
+ [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html)
+ [AWS IoT 1\-Click Programming Model](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-programming.html)