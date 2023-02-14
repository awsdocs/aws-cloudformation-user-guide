# AWS::Lex::Bot OutputContext<a name="aws-properties-lex-bot-outputcontext"></a>

Describes a session context that is activated when an intent is fulfilled\.

## Syntax<a name="aws-properties-lex-bot-outputcontext-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-outputcontext-syntax.json"></a>

```
{
  "[Name](#cfn-lex-bot-outputcontext-name)" : String,
  "[TimeToLiveInSeconds](#cfn-lex-bot-outputcontext-timetoliveinseconds)" : Integer,
  "[TurnsToLive](#cfn-lex-bot-outputcontext-turnstolive)" : Integer
}
```

### YAML<a name="aws-properties-lex-bot-outputcontext-syntax.yaml"></a>

```
  [Name](#cfn-lex-bot-outputcontext-name): String
  [TimeToLiveInSeconds](#cfn-lex-bot-outputcontext-timetoliveinseconds): Integer
  [TurnsToLive](#cfn-lex-bot-outputcontext-turnstolive): Integer
```

## Properties<a name="aws-properties-lex-bot-outputcontext-properties"></a>

`Name`  <a name="cfn-lex-bot-outputcontext-name"></a>
The name of the output context\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeToLiveInSeconds`  <a name="cfn-lex-bot-outputcontext-timetoliveinseconds"></a>
The amount of time, in seconds, that the output context should remain active\. The time is figured from the first time the context is sent to the user\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TurnsToLive`  <a name="cfn-lex-bot-outputcontext-turnstolive"></a>
The number of conversation turns that the output context should remain active\. The number of turns is counted from the first time that the context is sent to the user\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)