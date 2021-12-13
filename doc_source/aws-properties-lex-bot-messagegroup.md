# AWS::Lex::Bot MessageGroup<a name="aws-properties-lex-bot-messagegroup"></a>

Provides one or more messages that Amazon Lex should send to the user\.

## Syntax<a name="aws-properties-lex-bot-messagegroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-messagegroup-syntax.json"></a>

```
{
  "[Message](#cfn-lex-bot-messagegroup-message)" : Message,
  "[Variations](#cfn-lex-bot-messagegroup-variations)" : [ Message, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-messagegroup-syntax.yaml"></a>

```
  [Message](#cfn-lex-bot-messagegroup-message): 
    Message
  [Variations](#cfn-lex-bot-messagegroup-variations): 
    - Message
```

## Properties<a name="aws-properties-lex-bot-messagegroup-properties"></a>

`Message`  <a name="cfn-lex-bot-messagegroup-message"></a>
The primary message that Amazon Lex should send to the user\.  
*Required*: Yes  
*Type*: [Message](aws-properties-lex-bot-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variations`  <a name="cfn-lex-bot-messagegroup-variations"></a>
Message variations to send to the user\. When variations are defined, Amazon Lex chooses the primary message or one of the variations to send to the user\.  
*Required*: No  
*Type*: List of [Message](aws-properties-lex-bot-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)