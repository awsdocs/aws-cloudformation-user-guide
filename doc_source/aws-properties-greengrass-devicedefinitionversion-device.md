# AWS IoT Greengrass DeviceDefinitionVersion Device<a name="aws-properties-greengrass-devicedefinitionversion-device"></a>

<a name="aws-properties-greengrass-devicedefinitionversion-device-description"></a> A device is an AWS IoT device \(thing\) that's added to a Greengrass group\. Greengrass devices can communicate with the Greengrass core in the same group\. For more information, see [What Is AWS IoT Greengrass?](https://docs.aws.amazon.com/greengrass/latest/developerguide/what-is-gg.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-devicedefinitionversion-device-inheritance"></a> In an AWS CloudFormation template, the `Devices` property of the [AWS::Greengrass::DeviceDefinitionVersion](aws-resource-greengrass-devicedefinitionversion.md) resource contains a list of `Device` property types\.

## Syntax<a name="aws-properties-greengrass-devicedefinitionversion-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-devicedefinitionversion-device-syntax.json"></a>

```
{
  "[SyncShadow](#cfn-greengrass-devicedefinitionversion-device-syncshadow)" : Boolean,
  "[ThingArn](#cfn-greengrass-devicedefinitionversion-device-thingarn)" : String,
  "[Id](#cfn-greengrass-devicedefinitionversion-device-id)" : String,
  "[CertificateArn](#cfn-greengrass-devicedefinitionversion-device-certificatearn)" : String
}
```

### YAML<a name="aws-properties-greengrass-devicedefinitionversion-device-syntax.yaml"></a>

```
[SyncShadow](#cfn-greengrass-devicedefinitionversion-device-syncshadow): Boolean
[ThingArn](#cfn-greengrass-devicedefinitionversion-device-thingarn): String
[Id](#cfn-greengrass-devicedefinitionversion-device-id): String
[CertificateArn](#cfn-greengrass-devicedefinitionversion-device-certificatearn): String
```

## Properties<a name="aws-properties-greengrass-devicedefinitionversion-device-properties"></a>

`SyncShadow`  <a name="cfn-greengrass-devicedefinitionversion-device-syncshadow"></a>
Indicates whether the devices's local shadow is synced with the cloud automatically\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ThingArn`  <a name="cfn-greengrass-devicedefinitionversion-device-thingarn"></a>
The ARN of the device, which is an AWS IoT device \(thing\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Id`  <a name="cfn-greengrass-devicedefinitionversion-device-id"></a>
A descriptive or arbitrary ID for the device\. This value must be unique within the device definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CertificateArn`  <a name="cfn-greengrass-devicedefinitionversion-device-certificatearn"></a>
The ARN of the device certificate for the device\. This X\.509 certificate is used to authenticate the device with AWS IoT and AWS IoT Greengrass services\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-devicedefinitionversion-device-seealso"></a>
+ [Device](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-device.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)