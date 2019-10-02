# AWS::Greengrass::CoreDefinition CoreDefinitionVersion<a name="aws-properties-greengrass-coredefinition-coredefinitionversion"></a>

<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-description"></a> A core definition version contains a Greengrass [core](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-coredefinition-core.html)\.

**Note**  
After you create a core definition version that contains the core you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-inheritance"></a> In an AWS CloudFormation template, `CoreDefinitionVersion` is the property type of the `InitialVersion` property in the [ `AWS::Greengrass::CoreDefinition` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html) resource\.

## Syntax<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-syntax.json"></a>

```
{
  "[Cores](#cfn-greengrass-coredefinition-coredefinitionversion-cores)" : [ [Core](aws-properties-greengrass-coredefinition-core.md), ... ]
}
```

### YAML<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-syntax.yaml"></a>

```
  [Cores](#cfn-greengrass-coredefinition-coredefinitionversion-cores): 
    - [Core](aws-properties-greengrass-coredefinition-core.md)
```

## Properties<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-properties"></a>

`Cores`  <a name="cfn-greengrass-coredefinition-coredefinitionversion-cores"></a>
The Greengrass core in this version\. Currently, the `Cores` property for a core definition version can contain only one core\.  
*Required*: Yes  
*Type*: List of [Core](aws-properties-greengrass-coredefinition-core.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See Also<a name="aws-properties-greengrass-coredefinition-coredefinitionversion--seealso"></a>
+  [CoreDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-coredefinitionversion.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `cn-north-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-gov-west-1`
- `us-west-2`
