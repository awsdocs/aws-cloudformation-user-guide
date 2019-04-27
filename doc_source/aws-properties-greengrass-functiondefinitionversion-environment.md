# AWS IoT Greengrass FunctionDefinitionVersion Environment<a name="aws-properties-greengrass-functiondefinitionversion-environment"></a>

<a name="aws-properties-greengrass-functiondefinitionversion-environment-description"></a>The environment configuration for a Lambda function on the AWS IoT Greengrass core\.

<a name="aws-properties-greengrass-functiondefinitionversion-environment-inheritance"></a> In an AWS CloudFormation template, `Environment` is a property of the [FunctionConfiguration](aws-properties-greengrass-functiondefinitionversion-functionconfiguration.md) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinitionversion-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinitionversion-environment-syntax.json"></a>

```
{
  "[Variables](#cfn-greengrass-functiondefinitionversion-environment-variables)" : Json,
  "[Execution](#cfn-greengrass-functiondefinitionversion-environment-execution)" : [*Execution*](aws-properties-greengrass-functiondefinitionversion-execution.md),
  "[ResourceAccessPolicies](#cfn-greengrass-functiondefinitionversion-environment-resourceaccesspolicies)" : [ [*ResourceAccessPolicy*](aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy.md), ... ],
  "[AccessSysfs](#cfn-greengrass-functiondefinitionversion-environment-accesssysfs)" : Boolean
}
```

### YAML<a name="aws-properties-greengrass-functiondefinitionversion-environment-syntax.yaml"></a>

```
[Variables](#cfn-greengrass-functiondefinitionversion-environment-variables): Json
[Execution](#cfn-greengrass-functiondefinitionversion-environment-execution): 
  [*Execution*](aws-properties-greengrass-functiondefinitionversion-execution.md)
[ResourceAccessPolicies](#cfn-greengrass-functiondefinitionversion-environment-resourceaccesspolicies): 
  - [*ResourceAccessPolicy*](aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy.md)
[AccessSysfs](#cfn-greengrass-functiondefinitionversion-environment-accesssysfs): Boolean
```

## Properties<a name="aws-properties-greengrass-functiondefinitionversion-environment-properties"></a>

`Variables`  <a name="cfn-greengrass-functiondefinitionversion-environment-variables"></a>
Environment variables for the Lambda function\.  
 *Required*: No  
 *Type*: Json  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Execution`  <a name="cfn-greengrass-functiondefinitionversion-environment-execution"></a>
Settings for the Lambda execution environment in AWS IoT Greengrass\.  
 *Required*: No  
 *Type*: [Execution](aws-properties-greengrass-functiondefinitionversion-execution.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResourceAccessPolicies`  <a name="cfn-greengrass-functiondefinitionversion-environment-resourceaccesspolicies"></a>
A list of the [resources](aws-properties-greengrass-resourcedefinitionversion-resourceinstance.md) in the group that the function can access, with the corresponding read\-only or read\-write permissions\. The maximum is 10 resources\.  
This property applies only to Lambda functions that run in a Greengrass container\.
 *Required*: No  
 *Type*: List of [ResourceAccessPolicy](aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`AccessSysfs`  <a name="cfn-greengrass-functiondefinitionversion-environment-accesssysfs"></a>
Indicates whether the function is allowed to access the `/sys` directory on the core device, which allows the read device information from `/sys`\.  
This property applies only to Lambda functions that run in a Greengrass container\.
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-functiondefinitionversion-environment-seealso"></a>
+ [FunctionConfigurationEnvironment](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functionconfigurationenvironment.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)