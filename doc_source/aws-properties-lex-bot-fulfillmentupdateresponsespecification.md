# AWS::Lex::Bot FulfillmentUpdateResponseSpecification<a name="aws-properties-lex-bot-fulfillmentupdateresponsespecification"></a>

Provides settings for a message that is sent periodically to the user while a fulfillment Lambda function is running\.

## Syntax<a name="aws-properties-lex-bot-fulfillmentupdateresponsespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-fulfillmentupdateresponsespecification-syntax.json"></a>

```
{
  "[AllowInterrupt](#cfn-lex-bot-fulfillmentupdateresponsespecification-allowinterrupt)" : Boolean,
  "[FrequencyInSeconds](#cfn-lex-bot-fulfillmentupdateresponsespecification-frequencyinseconds)" : Integer,
  "[MessageGroups](#cfn-lex-bot-fulfillmentupdateresponsespecification-messagegroups)" : [ MessageGroup, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-fulfillmentupdateresponsespecification-syntax.yaml"></a>

```
  [AllowInterrupt](#cfn-lex-bot-fulfillmentupdateresponsespecification-allowinterrupt): Boolean
  [FrequencyInSeconds](#cfn-lex-bot-fulfillmentupdateresponsespecification-frequencyinseconds): Integer
  [MessageGroups](#cfn-lex-bot-fulfillmentupdateresponsespecification-messagegroups): 
    - MessageGroup
```

## Properties<a name="aws-properties-lex-bot-fulfillmentupdateresponsespecification-properties"></a>

`AllowInterrupt`  <a name="cfn-lex-bot-fulfillmentupdateresponsespecification-allowinterrupt"></a>
Determines whether the user can interrupt an update message while it is playing\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrequencyInSeconds`  <a name="cfn-lex-bot-fulfillmentupdateresponsespecification-frequencyinseconds"></a>
The frequency that a message is sent to the user\. When the period ends, Amazon Lex chooses a message from the message groups and plays it to the user\. If the fulfillment Lambda returns before the first period ends, an update message is not played to the user\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroups`  <a name="cfn-lex-bot-fulfillmentupdateresponsespecification-messagegroups"></a>
1 \- 5 message groups that contain update messages\. Amazon Lex chooses one of the messages to play to the user\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)