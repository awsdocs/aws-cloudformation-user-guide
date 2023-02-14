# AWS::Lex::BotAlias CodeHookSpecification<a name="aws-properties-lex-botalias-codehookspecification"></a>

Contains information about code hooks that Amazon Lex calls during a conversation\.

## Syntax<a name="aws-properties-lex-botalias-codehookspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-codehookspecification-syntax.json"></a>

```
{
  "[LambdaCodeHook](#cfn-lex-botalias-codehookspecification-lambdacodehook)" : LambdaCodeHook
}
```

### YAML<a name="aws-properties-lex-botalias-codehookspecification-syntax.yaml"></a>

```
  [LambdaCodeHook](#cfn-lex-botalias-codehookspecification-lambdacodehook): 
    LambdaCodeHook
```

## Properties<a name="aws-properties-lex-botalias-codehookspecification-properties"></a>

`LambdaCodeHook`  <a name="cfn-lex-botalias-codehookspecification-lambdacodehook"></a>
Specifies a Lambda function that verifies requests to a bot or fulfills the user's request to a bot\.  
*Required*: Yes  
*Type*: [LambdaCodeHook](aws-properties-lex-botalias-lambdacodehook.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)