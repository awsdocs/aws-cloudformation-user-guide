# AWS::Greengrass::FunctionDefinition Function<a name="aws-properties-greengrass-functiondefinition-function"></a>

<a name="aws-properties-greengrass-functiondefinition-function-description"></a>A function is a Lambda function that's referenced from an AWS IoT Greengrass group\. The function is deployed to a Greengrass core where it runs locally\. For more information, see [Run Lambda Functions on the AWS IoT Greengrass Core](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-functions.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-functiondefinition-function-inheritance"></a> In an AWS CloudFormation template, the `Functions` property of the [ `FunctionDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-functiondefinitionversion.html) property type contains a list of `Function` property types\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-function-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-function-syntax.json"></a>

```
{
  "[FunctionArn](#cfn-greengrass-functiondefinition-function-functionarn)" : String,
  "[FunctionConfiguration](#cfn-greengrass-functiondefinition-function-functionconfiguration)" : FunctionConfiguration,
  "[Id](#cfn-greengrass-functiondefinition-function-id)" : String
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-function-syntax.yaml"></a>

```
  [FunctionArn](#cfn-greengrass-functiondefinition-function-functionarn): String
  [FunctionConfiguration](#cfn-greengrass-functiondefinition-function-functionconfiguration): 
    FunctionConfiguration
  [Id](#cfn-greengrass-functiondefinition-function-id): String
```

## Properties<a name="aws-properties-greengrass-functiondefinition-function-properties"></a>

`FunctionArn`  <a name="cfn-greengrass-functiondefinition-function-functionarn"></a>
The Amazon Resource Name \(ARN\) of the alias \(recommended\) or version of the referenced Lambda function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FunctionConfiguration`  <a name="cfn-greengrass-functiondefinition-function-functionconfiguration"></a>
The group\-specific settings of the Lambda function\. These settings configure the function's behavior in the Greengrass group\.  
*Required*: Yes  
*Type*: [FunctionConfiguration](aws-properties-greengrass-functiondefinition-functionconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Id`  <a name="cfn-greengrass-functiondefinition-function-id"></a>
A descriptive or arbitrary ID for the function\. This value must be unique within the function definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-functiondefinition-function--seealso"></a>
+  [Function](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-function.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 