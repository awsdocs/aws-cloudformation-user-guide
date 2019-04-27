# AWS IoT Greengrass CoreDefinitionVersion Core<a name="aws-properties-greengrass-coredefinitionversion-core"></a>

<a name="aws-properties-greengrass-coredefinitionversion-core-description"></a> A core is an AWS IoT device that runs the AWS IoT Greengrass core software and manages local processes for a Greengrass group\. For more information, see [What Is AWS IoT Greengrass?](https://docs.aws.amazon.com/greengrass/latest/developerguide/what-is-gg.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-coredefinitionversion-core-inheritance"></a> In an AWS CloudFormation template, the `Cores` property of the [AWS::Greengrass::CoreDefinitionVersion](aws-resource-greengrass-coredefinitionversion.md) resource contains a list of `Core` property types\. Currently, the list can contain only one core\.

## Syntax<a name="aws-properties-greengrass-coredefinitionversion-core-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-coredefinitionversion-core-syntax.json"></a>

```
{
  "[SyncShadow](#cfn-greengrass-coredefinitionversion-core-syncshadow)" : Boolean,
  "[ThingArn](#cfn-greengrass-coredefinitionversion-core-thingarn)" : String,
  "[Id](#cfn-greengrass-coredefinitionversion-core-id)" : String,
  "[CertificateArn](#cfn-greengrass-coredefinitionversion-core-certificatearn)" : String
}
```

### YAML<a name="aws-properties-greengrass-coredefinitionversion-core-syntax.yaml"></a>

```
[SyncShadow](#cfn-greengrass-coredefinitionversion-core-syncshadow): Boolean
[ThingArn](#cfn-greengrass-coredefinitionversion-core-thingarn): String
[Id](#cfn-greengrass-coredefinitionversion-core-id): String
[CertificateArn](#cfn-greengrass-coredefinitionversion-core-certificatearn): String
```

## Properties<a name="aws-properties-greengrass-coredefinitionversion-core-properties"></a>

`SyncShadow`  <a name="cfn-greengrass-coredefinitionversion-core-syncshadow"></a>
Indicates whether the core's local shadow is synced with the cloud automatically\. The default is false\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ThingArn`  <a name="cfn-greengrass-coredefinitionversion-core-thingarn"></a>
The ARN of the core, which is an AWS IoT device \(thing\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Id`  <a name="cfn-greengrass-coredefinitionversion-core-id"></a>
A descriptive or arbitrary ID for the core\. This value must be unique within the core definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CertificateArn`  <a name="cfn-greengrass-coredefinitionversion-core-certificatearn"></a>
The ARN of the device certificate for the core\. This X\.509 certificate is used to authenticate the core with AWS IoT and AWS IoT Greengrass services\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-coredefinitionversion-core-seealso"></a>
+ [Core](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-core.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)