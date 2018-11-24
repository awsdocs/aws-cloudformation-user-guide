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
    "[Enabled](#cfn-iot1click-device-enabled)" : String
  }
}
```

### YAML<a name="aws-resource-iot1click-device-syntax.yaml"></a>

```
Type: "AWS::IoT1Click::Device"
Properties:
  [DeviceId](#cfn-iot1click-device-deviceid): String
  [Enabled](#cfn-iot1click-device-enabled): String
```

## Properties<a name="aws-resource-iot1click-device-properties"></a>

`DeviceId`  <a name="cfn-iot1click-device-deviceid"></a>
The unique identifier of the device\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Enabled`  <a name="cfn-iot1click-device-enabled"></a>
A Boolean value indicating whether the device is enabled \(`true`\) or not \(`false`\)\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-iot1click-device-returnvalues"></a>

### Ref<a name="aws-resource-iot1click-device-ref"></a>

When you pass the logical ID of an `AWS::IoT1Click::Device` resource to the intrinsic `Ref` function, the function returns the device ARN, such as `arn:aws:iot1click:us-west-2:123456789012:devices/G030PX0312744DWM`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-iot1click-device-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The ARN of the device, such as `arn:aws:iot1click:us-west-2:123456789012:devices/G030PX0312744DWM`\. 

`DeviceId`  
The ID of the device, such as `G030PX0312744DWM`\. 

`Enabled`  
A Boolean value indicating whether the device is enabled \(`true`\) or not \(`false`\)\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-iot1click-device-examples"></a>

The following example enables a device\.

### JSON<a name="aws-resource-iot1click-device-example1.json"></a>

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

### YAML<a name="aws-resource-iot1click-device-example1.yaml"></a>

```
SampleDevice:
  Type: "AWS::IoT1Click::Device"
  Properties:
    DeviceId: G030PX0312744DWM
    Enabled: True
```

## See Also<a name="aws-resource-iot1click-device-seealso"></a>
+ [Device](https://docs.aws.amazon.com/iot-1-click/1.0/devices-apireference/devices-deviceid.html)
+ [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html)
+ [AWS IoT 1\-Click Programming Model](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-programming.html)