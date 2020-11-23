# AWS::Greengrass::FunctionDefinition FunctionConfiguration<a name="aws-properties-greengrass-functiondefinition-functionconfiguration"></a>

<a name="aws-properties-greengrass-functiondefinition-functionconfiguration-description"></a>The group\-specific configuration settings for a Lambda function\. These settings configure the function's behavior in the Greengrass group\. For more information, see [Controlling Execution of Greengrass Lambda Functions by Using Group\-Specific Configuration](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-functiondefinition-functionconfiguration-inheritance"></a> In an AWS CloudFormation template, `FunctionConfiguration` is a property of the [ `Function` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-function.html) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-functionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-functionconfiguration-syntax.json"></a>

```
{
  "[EncodingType](#cfn-greengrass-functiondefinition-functionconfiguration-encodingtype)" : String,
  "[Environment](#cfn-greengrass-functiondefinition-functionconfiguration-environment)" : Environment,
  "[ExecArgs](#cfn-greengrass-functiondefinition-functionconfiguration-execargs)" : String,
  "[Executable](#cfn-greengrass-functiondefinition-functionconfiguration-executable)" : String,
  "[MemorySize](#cfn-greengrass-functiondefinition-functionconfiguration-memorysize)" : Integer,
  "[Pinned](#cfn-greengrass-functiondefinition-functionconfiguration-pinned)" : Boolean,
  "[Timeout](#cfn-greengrass-functiondefinition-functionconfiguration-timeout)" : Integer
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-functionconfiguration-syntax.yaml"></a>

```
  [EncodingType](#cfn-greengrass-functiondefinition-functionconfiguration-encodingtype): String
  [Environment](#cfn-greengrass-functiondefinition-functionconfiguration-environment): 
    Environment
  [ExecArgs](#cfn-greengrass-functiondefinition-functionconfiguration-execargs): String
  [Executable](#cfn-greengrass-functiondefinition-functionconfiguration-executable): String
  [MemorySize](#cfn-greengrass-functiondefinition-functionconfiguration-memorysize): Integer
  [Pinned](#cfn-greengrass-functiondefinition-functionconfiguration-pinned): Boolean
  [Timeout](#cfn-greengrass-functiondefinition-functionconfiguration-timeout): Integer
```

## Properties<a name="aws-properties-greengrass-functiondefinition-functionconfiguration-properties"></a>

`EncodingType`  <a name="cfn-greengrass-functiondefinition-functionconfiguration-encodingtype"></a>
The expected encoding type of the input payload for the function\. Valid values are `json` \(default\) and `binary`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Environment`  <a name="cfn-greengrass-functiondefinition-functionconfiguration-environment"></a>
The environment configuration of the function\.  
*Required*: No  
*Type*: [Environment](aws-properties-greengrass-functiondefinition-environment.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExecArgs`  <a name="cfn-greengrass-functiondefinition-functionconfiguration-execargs"></a>
The execution arguments\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Executable`  <a name="cfn-greengrass-functiondefinition-functionconfiguration-executable"></a>
The name of the function executable\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MemorySize`  <a name="cfn-greengrass-functiondefinition-functionconfiguration-memorysize"></a>
The memory size \(in KB\) required by the function\.  
This property applies only to Lambda functions that run in a Greengrass container\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Pinned`  <a name="cfn-greengrass-functiondefinition-functionconfiguration-pinned"></a>
Indicates whether the function is pinned \(or *long\-lived*\)\. Pinned functions start when the core starts and process all requests in the same container\. The default value is false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-greengrass-functiondefinition-functionconfiguration-timeout"></a>
The allowed execution time \(in seconds\) after which the function should terminate\. For pinned functions, this timeout applies for each request\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-functiondefinition-functionconfiguration--seealso"></a>
+  [FunctionConfiguration](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functionconfiguration.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 