# AWS IoT Greengrass DeviceDefinition Device<a name="aws-properties-greengrass-devicedefinition-device"></a>

<a name="aws-properties-greengrass-devicedefinition-device-description"></a> A device is an AWS IoT device \(thing\) that's added to a Greengrass group\. Greengrass devices can communicate with the Greengrass core in the same group\. For more information, see [What Is AWS IoT Greengrass?](https://docs.aws.amazon.com/greengrass/latest/developerguide/what-is-gg.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-devicedefinition-device-inheritance"></a> In an AWS CloudFormation template, the `Devices` property of the [AWS IoT Greengrass DeviceDefinition DeviceDefinitionVersion](aws-properties-greengrass-devicedefinition-devicedefinitionversion.md) property type contains a list of `Device` property types\.

## Syntax<a name="aws-properties-greengrass-devicedefinition-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-devicedefinition-device-syntax.json"></a>

```
{
  "[SyncShadow](#cfn-greengrass-devicedefinition-device-syncshadow)" : Boolean,
  "[ThingArn](#cfn-greengrass-devicedefinition-device-thingarn)" : String,
  "[Id](#cfn-greengrass-devicedefinition-device-id)" : String,
  "[CertificateArn](#cfn-greengrass-devicedefinition-device-certificatearn)" : String
}
```

### YAML<a name="aws-properties-greengrass-devicedefinition-device-syntax.yaml"></a>

```
[SyncShadow](#cfn-greengrass-devicedefinition-device-syncshadow): Boolean
[ThingArn](#cfn-greengrass-devicedefinition-device-thingarn): String
[Id](#cfn-greengrass-devicedefinition-device-id): String
[CertificateArn](#cfn-greengrass-devicedefinition-device-certificatearn): String
```

## Properties<a name="aws-properties-greengrass-devicedefinition-device-properties"></a>

`SyncShadow`  <a name="cfn-greengrass-devicedefinition-device-syncshadow"></a>
Indicates whether the device's local shadow is synced with the cloud automatically\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ThingArn`  <a name="cfn-greengrass-devicedefinition-device-thingarn"></a>
The ARN of the device, which is an AWS IoT device \(thing\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Id`  <a name="cfn-greengrass-devicedefinition-device-id"></a>
A descriptive or arbitrary ID for the device\. This value must be unique within the device definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CertificateArn`  <a name="cfn-greengrass-devicedefinition-device-certificatearn"></a>
The ARN of the device certificate for the device\. This X\.509 certificate is used to authenticate the device with AWS IoT and AWS IoT Greengrass services\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-devicedefinition-device-seealso"></a>
+ [Device](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-device.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)