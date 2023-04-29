# AWS::Lex::Bot FulfillmentStartResponseSpecification<a name="aws-properties-lex-bot-fulfillmentstartresponsespecification"></a>

<a name="aws-properties-lex-bot-fulfillmentstartresponsespecification-description"></a>The `FulfillmentStartResponseSpecification` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

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
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DelayInSeconds`  <a name="cfn-lex-bot-fulfillmentstartresponsespecification-delayinseconds"></a>
Property description not available\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroups`  <a name="cfn-lex-bot-fulfillmentstartresponsespecification-messagegroups"></a>
Property description not available\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)