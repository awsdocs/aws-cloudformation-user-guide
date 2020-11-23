# AWS::Greengrass::ResourceDefinition LocalVolumeResourceData<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata"></a>

<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata-description"></a>Settings for a local volume resource, which represents a file or directory on the root file system\. For more information, see [Access Local Resources with Lambda Functions](https://docs.aws.amazon.com/greengrass/latest/developerguide/access-local-resources.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata-inheritance"></a> In an AWS CloudFormation template, `LocalVolumeResourceData` can be used in the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-resourcedatacontainer.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-resourcedatacontainer.html) property type\.

## Syntax<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata-syntax.json"></a>

```
{
  "[DestinationPath](#cfn-greengrass-resourcedefinition-localvolumeresourcedata-destinationpath)" : String,
  "[GroupOwnerSetting](#cfn-greengrass-resourcedefinition-localvolumeresourcedata-groupownersetting)" : GroupOwnerSetting,
  "[SourcePath](#cfn-greengrass-resourcedefinition-localvolumeresourcedata-sourcepath)" : String
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata-syntax.yaml"></a>

```
  [DestinationPath](#cfn-greengrass-resourcedefinition-localvolumeresourcedata-destinationpath): String
  [GroupOwnerSetting](#cfn-greengrass-resourcedefinition-localvolumeresourcedata-groupownersetting): 
    GroupOwnerSetting
  [SourcePath](#cfn-greengrass-resourcedefinition-localvolumeresourcedata-sourcepath): String
```

## Properties<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata-properties"></a>

`DestinationPath`  <a name="cfn-greengrass-resourcedefinition-localvolumeresourcedata-destinationpath"></a>
The absolute local path of the resource in the Lambda environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupOwnerSetting`  <a name="cfn-greengrass-resourcedefinition-localvolumeresourcedata-groupownersetting"></a>
Settings that define additional Linux OS group permissions to give to the Lambda function process\.  
*Required*: No  
*Type*: [GroupOwnerSetting](aws-properties-greengrass-resourcedefinition-groupownersetting.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourcePath`  <a name="cfn-greengrass-resourcedefinition-localvolumeresourcedata-sourcepath"></a>
The local absolute path of the volume resource on the host\. The source path for a volume resource type cannot start with `/sys`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-resourcedefinition-localvolumeresourcedata--seealso"></a>
+  [LocalVolumeResourceData](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-localvolumeresourcedata.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 