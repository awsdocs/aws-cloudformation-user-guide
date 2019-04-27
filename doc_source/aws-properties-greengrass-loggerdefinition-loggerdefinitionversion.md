# AWS IoT Greengrass LoggerDefinition LoggerDefinitionVersion<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion"></a>

<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-description"></a> A logger definition version contains a list of [loggers](aws-properties-greengrass-loggerdefinition-logger.md)\.

**Note**  
After you create a logger definition version that contains the loggers you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-inheritance"></a> In an AWS CloudFormation template, `LoggerDefinitionVersion` is the property type of the `InitialVersion` property in the [AWS::Greengrass::LoggerDefinition](aws-resource-greengrass-loggerdefinition.md) resource\.

## Syntax<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-syntax.json"></a>

```
{
  "[Loggers](#cfn-greengrass-loggerdefinition-loggerdefinitionversion-loggers)" : [ [*Logger*](aws-properties-greengrass-loggerdefinition-logger.md), ... ]
}
```

### YAML<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-syntax.yaml"></a>

```
[Loggers](#cfn-greengrass-loggerdefinition-loggerdefinitionversion-loggers): 
  - [*Logger*](aws-properties-greengrass-loggerdefinition-logger.md)
```

## Properties<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-properties"></a>

`Loggers`  <a name="cfn-greengrass-loggerdefinition-loggerdefinitionversion-loggers"></a>
The loggers in this version\.  
 *Required*: Yes  
 *Type*: List of [Logger](aws-properties-greengrass-loggerdefinition-logger.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-seealso"></a>
+ [LoggerDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-loggerdefinitionversion.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)