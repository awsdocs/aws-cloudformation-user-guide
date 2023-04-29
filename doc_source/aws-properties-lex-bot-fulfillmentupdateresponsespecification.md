# AWS::Lex::Bot FulfillmentUpdateResponseSpecification<a name="aws-properties-lex-bot-fulfillmentupdateresponsespecification"></a>

<a name="aws-properties-lex-bot-fulfillmentupdateresponsespecification-description"></a>The `FulfillmentUpdateResponseSpecification` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

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
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrequencyInSeconds`  <a name="cfn-lex-bot-fulfillmentupdateresponsespecification-frequencyinseconds"></a>
Property description not available\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroups`  <a name="cfn-lex-bot-fulfillmentupdateresponsespecification-messagegroups"></a>
Property description not available\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)