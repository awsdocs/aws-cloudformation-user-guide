# AWS::Greengrass::FunctionDefinition Environment<a name="aws-properties-greengrass-functiondefinition-environment"></a>

<a name="aws-properties-greengrass-functiondefinition-environment-description"></a>The environment configuration for a Lambda function on the AWS IoT Greengrass core\.

<a name="aws-properties-greengrass-functiondefinition-environment-inheritance"></a> In an AWS CloudFormation template, `Environment` is a property of the [ `FunctionConfiguration` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-functionconfiguration.html) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-environment-syntax.json"></a>

```
{
  "[AccessSysfs](#cfn-greengrass-functiondefinition-environment-accesssysfs)" : Boolean,
  "[Execution](#cfn-greengrass-functiondefinition-environment-execution)" : Execution,
  "[ResourceAccessPolicies](#cfn-greengrass-functiondefinition-environment-resourceaccesspolicies)" : [ ResourceAccessPolicy, ... ],
  "[Variables](#cfn-greengrass-functiondefinition-environment-variables)" : Json
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-environment-syntax.yaml"></a>

```
  [AccessSysfs](#cfn-greengrass-functiondefinition-environment-accesssysfs): Boolean
  [Execution](#cfn-greengrass-functiondefinition-environment-execution): 
    Execution
  [ResourceAccessPolicies](#cfn-greengrass-functiondefinition-environment-resourceaccesspolicies): 
    - ResourceAccessPolicy
  [Variables](#cfn-greengrass-functiondefinition-environment-variables): Json
```

## Properties<a name="aws-properties-greengrass-functiondefinition-environment-properties"></a>

`AccessSysfs`  <a name="cfn-greengrass-functiondefinition-environment-accesssysfs"></a>
Indicates whether the function is allowed to access the `/sys` directory on the core device, which allows the read device information from `/sys`\.  
This property applies only to Lambda functions that run in a Greengrass container\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Execution`  <a name="cfn-greengrass-functiondefinition-environment-execution"></a>
Settings for the Lambda execution environment in AWS IoT Greengrass\.  
*Required*: No  
*Type*: [Execution](aws-properties-greengrass-functiondefinition-execution.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceAccessPolicies`  <a name="cfn-greengrass-functiondefinition-environment-resourceaccesspolicies"></a>
A list of the [resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-resourceinstance.html) in the group that the function can access, with the corresponding read\-only or read\-write permissions\. The maximum is 10 resources\.  
This property applies only for Lambda functions that run in a Greengrass container\.
*Required*: No  
*Type*: List of [ResourceAccessPolicy](aws-properties-greengrass-functiondefinition-resourceaccesspolicy.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Variables`  <a name="cfn-greengrass-functiondefinition-environment-variables"></a>
Environment variables for the Lambda function\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-functiondefinition-environment--seealso"></a>
+  [FunctionConfigurationEnvironment](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functionconfigurationenvironment.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 