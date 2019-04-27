# AWS IoT Greengrass CoreDefinition CoreDefinitionVersion<a name="aws-properties-greengrass-coredefinition-coredefinitionversion"></a>

<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-description"></a> A core definition version contains a Greengrass [core](aws-properties-greengrass-coredefinition-core.md)\.

**Note**  
After you create a core definition version that contains the core you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-inheritance"></a> In an AWS CloudFormation template, `CoreDefinitionVersion` is the property type of the `InitialVersion` property in the [AWS::Greengrass::CoreDefinition](aws-resource-greengrass-coredefinition.md) resource\.

## Syntax<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-syntax.json"></a>

```
{
  "[Cores](#cfn-greengrass-coredefinition-coredefinitionversion-cores)" : [ [*Core*](aws-properties-greengrass-coredefinition-core.md) ]
}
```

### YAML<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-syntax.yaml"></a>

```
[Cores](#cfn-greengrass-coredefinition-coredefinitionversion-cores): 
  - [*Core*](aws-properties-greengrass-coredefinition-core.md)
```

## Properties<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-properties"></a>

`Cores`  <a name="cfn-greengrass-coredefinition-coredefinitionversion-cores"></a>
The Greengrass core in this version\. Currently, a core definition version can contain only one core\.  
 *Required*: Yes  
 *Type*: List of [Core](aws-properties-greengrass-coredefinition-core.md) property types\. This list must contain exactly one `Core`\.  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-coredefinition-coredefinitionversion-seealso"></a>
+ [CoreDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-coredefinitionversion.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)