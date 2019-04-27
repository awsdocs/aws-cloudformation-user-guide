# AWS IoT Greengrass FunctionDefinition DefaultConfig<a name="aws-properties-greengrass-functiondefinition-defaultconfig"></a>

<a name="aws-properties-greengrass-functiondefinition-defaultconfig-description"></a>The default configuration that applies to all Lambda functions in the function definition version\. Individual Lambda functions can override these settings\.

<a name="aws-properties-greengrass-functiondefinition-defaultconfig-inheritance"></a> In an AWS CloudFormation template, `DefaultConfig` is a property of the [FunctionDefinitionVersion](aws-properties-greengrass-functiondefinition-functiondefinitionversion.md) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax.json"></a>

```
{
  "[Execution](#cfn-greengrass-functiondefinition-defaultconfig-execution)" : [*Execution*](aws-properties-greengrass-functiondefinition-execution.md)
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax.yaml"></a>

```
[Execution](#cfn-greengrass-functiondefinition-defaultconfig-execution): 
  [*Execution*](aws-properties-greengrass-functiondefinition-execution.md)
```

## Properties<a name="aws-properties-greengrass-functiondefinition-defaultconfig-properties"></a>

`Execution`  <a name="cfn-greengrass-functiondefinition-defaultconfig-execution"></a>
Configuration settings for the Lambda execution environment on the AWS IoT Greengrass core\.  
 *Required*: Yes  
 *Type*: [Execution](aws-properties-greengrass-functiondefinition-execution.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-greengrass-functiondefinition-defaultconfig-seealso"></a>
+ [FunctionConfigurationEnvironment](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functionconfigurationenvironment.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)