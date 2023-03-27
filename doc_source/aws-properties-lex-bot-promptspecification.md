# AWS::Lex::Bot PromptSpecification<a name="aws-properties-lex-bot-promptspecification"></a>

Specifies a list of message groups that Amazon Lex sends to a user to elicit a response\.

## Syntax<a name="aws-properties-lex-bot-promptspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-promptspecification-syntax.json"></a>

```
{
  "[AllowInterrupt](#cfn-lex-bot-promptspecification-allowinterrupt)" : Boolean,
  "[MaxRetries](#cfn-lex-bot-promptspecification-maxretries)" : Integer,
  "[MessageGroupsList](#cfn-lex-bot-promptspecification-messagegroupslist)" : [ MessageGroup, ... ],
  "[MessageSelectionStrategy](#cfn-lex-bot-promptspecification-messageselectionstrategy)" : String,
  "[PromptAttemptsSpecification](#cfn-lex-bot-promptspecification-promptattemptsspecification)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-lex-bot-promptspecification-syntax.yaml"></a>

```
  [AllowInterrupt](#cfn-lex-bot-promptspecification-allowinterrupt): Boolean
  [MaxRetries](#cfn-lex-bot-promptspecification-maxretries): Integer
  [MessageGroupsList](#cfn-lex-bot-promptspecification-messagegroupslist): 
    - MessageGroup
  [MessageSelectionStrategy](#cfn-lex-bot-promptspecification-messageselectionstrategy): String
  [PromptAttemptsSpecification](#cfn-lex-bot-promptspecification-promptattemptsspecification): 
    Key : Value
```

## Properties<a name="aws-properties-lex-bot-promptspecification-properties"></a>

`AllowInterrupt`  <a name="cfn-lex-bot-promptspecification-allowinterrupt"></a>
Indicates whether the user can interrupt a speech prompt from the bot\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetries`  <a name="cfn-lex-bot-promptspecification-maxretries"></a>
The maximum number of times the bot tries to elicit a response from the user using this prompt\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroupsList`  <a name="cfn-lex-bot-promptspecification-messagegroupslist"></a>
A collection of messages that Amazon Lex can send to the user\. Amazon Lex chooses the actual message to send at runtime\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageSelectionStrategy`  <a name="cfn-lex-bot-promptspecification-messageselectionstrategy"></a>
Indicates how a message is selected from a message group among retries\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromptAttemptsSpecification`  <a name="cfn-lex-bot-promptspecification-promptattemptsspecification"></a>
Specifies the advanced settings on each attempt of the prompt\.  
*Required*: No  
*Type*: Map of [PromptAttemptSpecification](aws-properties-lex-bot-promptattemptspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)