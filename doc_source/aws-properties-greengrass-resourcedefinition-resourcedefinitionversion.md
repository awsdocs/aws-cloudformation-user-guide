# AWS IoT Greengrass ResourceDefinition ResourceDefinitionVersion<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion"></a>

<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion-description"></a>A resource definition version contains a list of resources\. \(In AWS CloudFormation, resources are named *resource instances*\.\)

**Note**  
After you create a resource definition version that contains the resources you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion-inheritance"></a> In an AWS CloudFormation template, `ResourceDefinitionVersion` is the property type of the `InitialVersion` property in the [AWS::Greengrass::ResourceDefinition](aws-resource-greengrass-resourcedefinition.md) resource\.

## Syntax<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion-syntax.json"></a>

```
{
  "[Resources](#cfn-greengrass-resourcedefinition-resourcedefinitionversion-resources)" : [ [*ResourceInstance*](aws-properties-greengrass-resourcedefinition-resourceinstance.md), ... ]
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion-syntax.yaml"></a>

```
[Resources](#cfn-greengrass-resourcedefinition-resourcedefinitionversion-resources): 
  - [*ResourceInstance*](aws-properties-greengrass-resourcedefinition-resourceinstance.md)
```

## Properties<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion-properties"></a>

`Resources`  <a name="cfn-greengrass-resourcedefinition-resourcedefinitionversion-resources"></a>
The resources in this version\.  
 *Required*: Yes  
 *Type*: List of [ResourceInstance](aws-properties-greengrass-resourcedefinition-resourceinstance.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-resourcedefinition-resourcedefinitionversion-seealso"></a>
+ [ResourceDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-resourcedefinitionversion.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)