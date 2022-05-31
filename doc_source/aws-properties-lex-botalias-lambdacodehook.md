# AWS::Lex::BotAlias LambdaCodeHook<a name="aws-properties-lex-botalias-lambdacodehook"></a>

Specifies a Lambda function that verifies requests to a bot or fulfills the user's request to a bot\.

## Syntax<a name="aws-properties-lex-botalias-lambdacodehook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-lambdacodehook-syntax.json"></a>

```
{
  "[CodeHookInterfaceVersion](#cfn-lex-botalias-lambdacodehook-codehookinterfaceversion)" : String,
  "[LambdaArn](#cfn-lex-botalias-lambdacodehook-lambdaarn)" : String
}
```

### YAML<a name="aws-properties-lex-botalias-lambdacodehook-syntax.yaml"></a>

```
  [CodeHookInterfaceVersion](#cfn-lex-botalias-lambdacodehook-codehookinterfaceversion): String
  [LambdaArn](#cfn-lex-botalias-lambdacodehook-lambdaarn): String
```

## Properties<a name="aws-properties-lex-botalias-lambdacodehook-properties"></a>

`CodeHookInterfaceVersion`  <a name="cfn-lex-botalias-lambdacodehook-codehookinterfaceversion"></a>
The version of the request\-response that you want Amazon Lex to use to invoke your Lambda function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaArn`  <a name="cfn-lex-botalias-lambdacodehook-lambdaarn"></a>
The Amazon Resource Name \(ARN\) of the Lambda function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)