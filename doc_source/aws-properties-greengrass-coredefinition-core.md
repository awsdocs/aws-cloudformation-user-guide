# AWS::Greengrass::CoreDefinition Core<a name="aws-properties-greengrass-coredefinition-core"></a>

<a name="aws-properties-greengrass-coredefinition-core-description"></a> A core is an AWS IoT device that runs the AWS IoT Greengrass core software and manages local processes for a Greengrass group\. For more information, see [What Is AWS IoT Greengrass?](https://docs.aws.amazon.com/greengrass/latest/developerguide/what-is-gg.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-coredefinition-core-inheritance"></a> In an AWS CloudFormation template, the `Cores` property of the [ `CoreDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-coredefinition-coredefinitionversion.html) property type contains a list of `Core` property types\. Currently, the list can contain only one core\.

## Syntax<a name="aws-properties-greengrass-coredefinition-core-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-coredefinition-core-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-greengrass-coredefinition-core-certificatearn)" : String,
  "[Id](#cfn-greengrass-coredefinition-core-id)" : String,
  "[SyncShadow](#cfn-greengrass-coredefinition-core-syncshadow)" : Boolean,
  "[ThingArn](#cfn-greengrass-coredefinition-core-thingarn)" : String
}
```

### YAML<a name="aws-properties-greengrass-coredefinition-core-syntax.yaml"></a>

```
  [CertificateArn](#cfn-greengrass-coredefinition-core-certificatearn): String
  [Id](#cfn-greengrass-coredefinition-core-id): String
  [SyncShadow](#cfn-greengrass-coredefinition-core-syncshadow): Boolean
  [ThingArn](#cfn-greengrass-coredefinition-core-thingarn): String
```

## Properties<a name="aws-properties-greengrass-coredefinition-core-properties"></a>

`CertificateArn`  <a name="cfn-greengrass-coredefinition-core-certificatearn"></a>
The Amazon Resource Name \(ARN\) of the device certificate for the core\. This X\.509 certificate is used to authenticate the core with AWS IoT and AWS IoT Greengrass services\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Id`  <a name="cfn-greengrass-coredefinition-core-id"></a>
A descriptive or arbitrary ID for the core\. This value must be unique within the core definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SyncShadow`  <a name="cfn-greengrass-coredefinition-core-syncshadow"></a>
Indicates whether the core's local shadow is synced with the cloud automatically\. The default is false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ThingArn`  <a name="cfn-greengrass-coredefinition-core-thingarn"></a>
The ARN of the core, which is an AWS IoT device \(thing\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-coredefinition-core--seealso"></a>
+  [Core](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-core.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 