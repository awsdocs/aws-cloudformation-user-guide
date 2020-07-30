# AWS::Greengrass::LoggerDefinition LoggerDefinitionVersion<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion"></a>

<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-description"></a> A logger definition version contains a list of [loggers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-loggerdefinition-logger.html)\.

**Note**  
After you create a logger definition version that contains the loggers you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-inheritance"></a> In an AWS CloudFormation template, `LoggerDefinitionVersion` is the property type of the `InitialVersion` property in the [ `AWS::Greengrass::LoggerDefinition` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html) resource\.

## Syntax<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-syntax.json"></a>

```
{
  "[Loggers](#cfn-greengrass-loggerdefinition-loggerdefinitionversion-loggers)" : [ Logger, ... ]
}
```

### YAML<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-syntax.yaml"></a>

```
  [Loggers](#cfn-greengrass-loggerdefinition-loggerdefinitionversion-loggers): 
    - Logger
```

## Properties<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion-properties"></a>

`Loggers`  <a name="cfn-greengrass-loggerdefinition-loggerdefinitionversion-loggers"></a>
The loggers in this version\.  
*Required*: Yes  
*Type*: List of [Logger](aws-properties-greengrass-loggerdefinition-logger.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-loggerdefinition-loggerdefinitionversion--seealso"></a>
+  [LoggerDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-loggerdefinitionversion.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 