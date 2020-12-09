# AWS::Greengrass::FunctionDefinition DefaultConfig<a name="aws-properties-greengrass-functiondefinition-defaultconfig"></a>

<a name="aws-properties-greengrass-functiondefinition-defaultconfig-description"></a>The default configuration that applies to all Lambda functions in the function definition version\. Individual Lambda functions can override these settings\.

<a name="aws-properties-greengrass-functiondefinition-defaultconfig-inheritance"></a> In an AWS CloudFormation template, `DefaultConfig` is a property of the [ `FunctionDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-functiondefinitionversion.html) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax.json"></a>

```
{
  "[Execution](#cfn-greengrass-functiondefinition-defaultconfig-execution)" : Execution
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax.yaml"></a>

```
  [Execution](#cfn-greengrass-functiondefinition-defaultconfig-execution): 
    Execution
```

## Properties<a name="aws-properties-greengrass-functiondefinition-defaultconfig-properties"></a>

`Execution`  <a name="cfn-greengrass-functiondefinition-defaultconfig-execution"></a>
Configuration settings for the Lambda execution environment on the AWS IoT Greengrass core\.  
*Required*: Yes  
*Type*: [Execution](aws-properties-greengrass-functiondefinition-execution.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-greengrass-functiondefinition-defaultconfig--seealso"></a>
+  [FunctionDefaultConfig](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functiondefaultconfig.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 