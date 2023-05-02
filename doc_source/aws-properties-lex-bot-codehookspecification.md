# AWS::Lex::Bot CodeHookSpecification<a name="aws-properties-lex-bot-codehookspecification"></a>

Contains information about code hooks that Amazon Lex calls during a conversation\.

## Syntax<a name="aws-properties-lex-bot-codehookspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-codehookspecification-syntax.json"></a>

```
{
  "[LambdaCodeHook](#cfn-lex-bot-codehookspecification-lambdacodehook)" : LambdaCodeHook
}
```

### YAML<a name="aws-properties-lex-bot-codehookspecification-syntax.yaml"></a>

```
  [LambdaCodeHook](#cfn-lex-bot-codehookspecification-lambdacodehook): 
    LambdaCodeHook
```

## Properties<a name="aws-properties-lex-bot-codehookspecification-properties"></a>

`LambdaCodeHook`  <a name="cfn-lex-bot-codehookspecification-lambdacodehook"></a>
Specifies a Lambda function that verifies requests to a bot or fulfills the user's request to a bot\.  
*Required*: Yes  
*Type*: [LambdaCodeHook](aws-properties-lex-bot-lambdacodehook.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)