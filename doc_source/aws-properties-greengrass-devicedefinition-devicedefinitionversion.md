# AWS::Greengrass::DeviceDefinition DeviceDefinitionVersion<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion"></a>

<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion-description"></a> A device definition version contains a list of [devices](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-devicedefinition-device.html)\.

**Note**  
After you create a device definition version that contains the devices you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion-inheritance"></a> In an AWS CloudFormation template, `DeviceDefinitionVersion` is the property type of the `InitialVersion` property in the [ `AWS::Greengrass::DeviceDefinition` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html) resource\.

## Syntax<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion-syntax.json"></a>

```
{
  "[Devices](#cfn-greengrass-devicedefinition-devicedefinitionversion-devices)" : [ Device, ... ]
}
```

### YAML<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion-syntax.yaml"></a>

```
  [Devices](#cfn-greengrass-devicedefinition-devicedefinitionversion-devices): 
    - Device
```

## Properties<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion-properties"></a>

`Devices`  <a name="cfn-greengrass-devicedefinition-devicedefinitionversion-devices"></a>
The devices in this version\.  
*Required*: Yes  
*Type*: List of [Device](aws-properties-greengrass-devicedefinition-device.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-devicedefinition-devicedefinitionversion--seealso"></a>
+  [DeviceDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-devicedefinitionversion.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 