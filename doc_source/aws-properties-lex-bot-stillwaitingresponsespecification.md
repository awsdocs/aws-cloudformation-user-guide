# AWS::Lex::Bot StillWaitingResponseSpecification<a name="aws-properties-lex-bot-stillwaitingresponsespecification"></a>

<a name="aws-properties-lex-bot-stillwaitingresponsespecification-description"></a>The `StillWaitingResponseSpecification` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

## Syntax<a name="aws-properties-lex-bot-stillwaitingresponsespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-stillwaitingresponsespecification-syntax.json"></a>

```
{
  "[AllowInterrupt](#cfn-lex-bot-stillwaitingresponsespecification-allowinterrupt)" : Boolean,
  "[FrequencyInSeconds](#cfn-lex-bot-stillwaitingresponsespecification-frequencyinseconds)" : Integer,
  "[MessageGroupsList](#cfn-lex-bot-stillwaitingresponsespecification-messagegroupslist)" : [ MessageGroup, ... ],
  "[TimeoutInSeconds](#cfn-lex-bot-stillwaitingresponsespecification-timeoutinseconds)" : Integer
}
```

### YAML<a name="aws-properties-lex-bot-stillwaitingresponsespecification-syntax.yaml"></a>

```
  [AllowInterrupt](#cfn-lex-bot-stillwaitingresponsespecification-allowinterrupt): Boolean
  [FrequencyInSeconds](#cfn-lex-bot-stillwaitingresponsespecification-frequencyinseconds): Integer
  [MessageGroupsList](#cfn-lex-bot-stillwaitingresponsespecification-messagegroupslist): 
    - MessageGroup
  [TimeoutInSeconds](#cfn-lex-bot-stillwaitingresponsespecification-timeoutinseconds): Integer
```

## Properties<a name="aws-properties-lex-bot-stillwaitingresponsespecification-properties"></a>

`AllowInterrupt`  <a name="cfn-lex-bot-stillwaitingresponsespecification-allowinterrupt"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrequencyInSeconds`  <a name="cfn-lex-bot-stillwaitingresponsespecification-frequencyinseconds"></a>
Property description not available\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroupsList`  <a name="cfn-lex-bot-stillwaitingresponsespecification-messagegroupslist"></a>
Property description not available\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInSeconds`  <a name="cfn-lex-bot-stillwaitingresponsespecification-timeoutinseconds"></a>
Property description not available\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)