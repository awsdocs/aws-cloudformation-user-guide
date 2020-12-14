# AWS::Greengrass::ResourceDefinitionVersion GroupOwnerSetting<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting"></a>

<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-description"></a>Settings that define additional Linux OS group permissions to give to the Lambda function process\. You can give the permissions of the Linux group that owns the resource or choose another Linux group\. These permissions are in addition to the function's `RunAs` permissions\.

<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting-inheritance"></a> In an AWS CloudFormation template, `GroupOwnerSetting` is a property of the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-localdeviceresourcedata.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-localdeviceresourcedata.html) and [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-localvolumeresourcedata.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-localvolumeresourcedata.html) property types\.

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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupOwner`  <a name="cfn-greengrass-resourcedefinitionversion-groupownersetting-groupowner"></a>
The name of the Linux group whose privileges you want to add to the Lambda process\. This value is ignored if `AutoAddGroupOwner` is true\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-resourcedefinitionversion-groupownersetting--seealso"></a>
+  [GroupOwnerSetting](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-groupownersetting.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 