# AWS::Greengrass::FunctionDefinition DefaultConfig<a name="aws-properties-greengrass-functiondefinition-defaultconfig"></a>

<a name="aws-properties-greengrass-functiondefinition-defaultconfig-description"></a>The default configuration that applies to all Lambda functions in the function definition version\. Individual Lambda functions can override these settings\.

<a name="aws-properties-greengrass-functiondefinition-defaultconfig-inheritance"></a> In an AWS CloudFormation template, `DefaultConfig` is a property of the [ `FunctionDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-functiondefinitionversion.html) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax.json"></a>

```
{
  "[Execution](#cfn-greengrass-functiondefinition-defaultconfig-execution)" : [Execution](aws-properties-greengrass-functiondefinition-execution.md)
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-defaultconfig-syntax.yaml"></a>

```
  [Execution](#cfn-greengrass-functiondefinition-defaultconfig-execution): 
    [Execution](aws-properties-greengrass-functiondefinition-execution.md)
```

## Properties<a name="aws-properties-greengrass-functiondefinition-defaultconfig-properties"></a>

`Execution`  <a name="cfn-greengrass-functiondefinition-defaultconfig-execution"></a>
Configuration settings for the Lambda execution environment on the AWS IoT Greengrass core\.  
*Required*: Yes  
*Type*: [Execution](aws-properties-greengrass-functiondefinition-execution.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-greengrass-functiondefinition-defaultconfig--seealso"></a>
+  [FunctionDefaultConfig](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functiondefaultconfig.html) in the * AWS IoT Greengrass API Reference * 
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
