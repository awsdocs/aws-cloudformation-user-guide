# AWS::Lex::Bot FulfillmentStartResponseSpecification<a name="aws-properties-lex-bot-fulfillmentstartresponsespecification"></a>

Provides settings for a message that is sent to the user when a fulfillment Lambda function starts running\.

## Syntax<a name="aws-properties-lex-bot-fulfillmentstartresponsespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-fulfillmentstartresponsespecification-syntax.json"></a>

```
{
  "[AllowInterrupt](#cfn-lex-bot-fulfillmentstartresponsespecification-allowinterrupt)" : Boolean,
  "[DelayInSeconds](#cfn-lex-bot-fulfillmentstartresponsespecification-delayinseconds)" : Integer,
  "[MessageGroups](#cfn-lex-bot-fulfillmentstartresponsespecification-messagegroups)" : [ MessageGroup, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-fulfillmentstartresponsespecification-syntax.yaml"></a>

```
  [AllowInterrupt](#cfn-lex-bot-fulfillmentstartresponsespecification-allowinterrupt): Boolean
  [DelayInSeconds](#cfn-lex-bot-fulfillmentstartresponsespecification-delayinseconds): Integer
  [MessageGroups](#cfn-lex-bot-fulfillmentstartresponsespecification-messagegroups): 
    - MessageGroup
```

## Properties<a name="aws-properties-lex-bot-fulfillmentstartresponsespecification-properties"></a>

`AllowInterrupt`  <a name="cfn-lex-bot-fulfillmentstartresponsespecification-allowinterrupt"></a>
Determines whether the user can interrupt the start message while it is playing\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DelayInSeconds`  <a name="cfn-lex-bot-fulfillmentstartresponsespecification-delayinseconds"></a>
The delay between when the Lambda fulfillment function starts running and the start message is played\. If the Lambda function returns before the delay is over, the start message isn't played\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroups`  <a name="cfn-lex-bot-fulfillmentstartresponsespecification-messagegroups"></a>
1 \- 5 message groups that contain start messages\. Amazon Lex chooses one of the messages to play to the user\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)