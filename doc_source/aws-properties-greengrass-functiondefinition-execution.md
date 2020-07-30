# AWS::Greengrass::FunctionDefinition Execution<a name="aws-properties-greengrass-functiondefinition-execution"></a>

<a name="aws-properties-greengrass-functiondefinition-execution-description"></a>Configuration settings for the Lambda execution environment on the AWS IoT Greengrass core\.

<a name="aws-properties-greengrass-functiondefinition-execution-inheritance"></a> In an AWS CloudFormation template, `Execution` is a property of the [ `DefaultConfig` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-defaultconfig.html) property type for a function definition version and the [ `Environment` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-environment.html) property type for a function\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-execution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-execution-syntax.json"></a>

```
{
  "[IsolationMode](#cfn-greengrass-functiondefinition-execution-isolationmode)" : String,
  "[RunAs](#cfn-greengrass-functiondefinition-execution-runas)" : RunAs
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-execution-syntax.yaml"></a>

```
  [IsolationMode](#cfn-greengrass-functiondefinition-execution-isolationmode): String
  [RunAs](#cfn-greengrass-functiondefinition-execution-runas): 
    RunAs
```

## Properties<a name="aws-properties-greengrass-functiondefinition-execution-properties"></a>

`IsolationMode`  <a name="cfn-greengrass-functiondefinition-execution-isolationmode"></a>
The containerization that the Lambda function runs in\. Valid values are `GreengrassContainer` or `NoContainer`\. Typically, this is `GreengrassContainer`\. For more information, see [Containerization](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html#lambda-function-containerization) in the *AWS IoT Greengrass Developer Guide*\.  
+ When set on the [ `DefaultConfig` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinitionversion-defaultconfig.html) property of a function definition version, this setting is used as the default containerization for all Lambda functions in the function definition version\.
+ When set on the [ `Environment` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinitionversion-environment.html) property of a function, this setting applies to the individual function and overrides the default\. Omit this value to run the function with the default containerization\.
We recommend that you run in a Greengrass container unless your business case requires that you run without containerization\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RunAs`  <a name="cfn-greengrass-functiondefinition-execution-runas"></a>
The user and group permissions used to run the Lambda function\. Typically, this is the ggc\_user and ggc\_group\. For more information, see [Run as](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html#lambda-access-identity.html) in the *AWS IoT Greengrass Developer Guide*\.  
+ When set on the [ `DefaultConfig` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinitionversion-defaultconfig.html) property of a function definition version, this setting is used as the default access identity for all Lambda functions in the function definition version\.
+ When set on the [ `Environment` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinitionversion-environment.html) property of a function, this setting applies to the individual function and overrides the default\. You can override the user, group, or both\. Omit this value to run the function with the default permissions\.
Running as the root user increases risks to your data and device\. Do not run as root \(UID/GID=0\) unless your business case requires it\. For more information and requirements, see [Running a Lambda Function as Root](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html#lambda-running-as-root)\. 
*Required*: No  
*Type*: [RunAs](aws-properties-greengrass-functiondefinition-runas.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-functiondefinition-execution--seealso"></a>
+  [FunctionExecutionConfig](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functionexecutionconfig.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 