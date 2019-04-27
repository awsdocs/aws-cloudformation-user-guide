# AWS IoT Greengrass ResourceDefinitionVersion GroupOwnerSetting<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting"></a>

<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-description"></a>Settings that define additional Linux OS group permissions to give to the Lambda function process\. You can give the permissions of the Linux group that owns the resource or choose another Linux group\. These permissions are in addition to the function's `RunAs` permissions\.

<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-inheritance"></a> In an AWS CloudFormation template, `GroupOwnerSetting` is a property of the [LocalDeviceResourceData](aws-properties-greengrass-resourcedefinitionversion-localdeviceresourcedata.md) and [LocalVolumeResourceData](aws-properties-greengrass-resourcedefinitionversion-localvolumeresourcedata.md) property types\.

## Syntax<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-syntax.json"></a>

```
{
  "[AutoAddGroupOwner](#cfn-greengrass-resourcedefinitionversion-groupownersetting-autoaddgroupowner)" : Boolean,
  "[GroupOwner](#cfn-greengrass-resourcedefinitionversion-groupownersetting-groupowner)" : String
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-syntax.yaml"></a>

```
[AutoAddGroupOwner](#cfn-greengrass-resourcedefinitionversion-groupownersetting-autoaddgroupowner): Boolean
[GroupOwner](#cfn-greengrass-resourcedefinitionversion-groupownersetting-groupowner): String
```

## Properties<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-properties"></a>

`AutoAddGroupOwner`  <a name="cfn-greengrass-resourcedefinitionversion-groupownersetting-autoaddgroupowner"></a>
Indicates whether to give the privileges of the Linux group that owns the resource to the Lambda process\. This gives the Lambda process the file access permissions of the Linux group\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`GroupOwner`  <a name="cfn-greengrass-resourcedefinitionversion-groupownersetting-groupowner"></a>
The name of the Linux group whose privileges you want to add to the Lambda process\. This value is ignored if `AutoAddGroupOwner` is true\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-seealso"></a>
+ [GroupOwnerSetting](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-groupownersetting.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)