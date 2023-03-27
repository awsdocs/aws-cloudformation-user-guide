# AWS::Lex::Bot WaitAndContinueSpecification<a name="aws-properties-lex-bot-waitandcontinuespecification"></a>

Specifies the prompts that Amazon Lex uses while a bot is waiting for customer input\. 

## Syntax<a name="aws-properties-lex-bot-waitandcontinuespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-waitandcontinuespecification-syntax.json"></a>

```
{
  "[ContinueResponse](#cfn-lex-bot-waitandcontinuespecification-continueresponse)" : ResponseSpecification,
  "[IsActive](#cfn-lex-bot-waitandcontinuespecification-isactive)" : Boolean,
  "[StillWaitingResponse](#cfn-lex-bot-waitandcontinuespecification-stillwaitingresponse)" : StillWaitingResponseSpecification,
  "[WaitingResponse](#cfn-lex-bot-waitandcontinuespecification-waitingresponse)" : ResponseSpecification
}
```

### YAML<a name="aws-properties-lex-bot-waitandcontinuespecification-syntax.yaml"></a>

```
  [ContinueResponse](#cfn-lex-bot-waitandcontinuespecification-continueresponse): 
    ResponseSpecification
  [IsActive](#cfn-lex-bot-waitandcontinuespecification-isactive): Boolean
  [StillWaitingResponse](#cfn-lex-bot-waitandcontinuespecification-stillwaitingresponse): 
    StillWaitingResponseSpecification
  [WaitingResponse](#cfn-lex-bot-waitandcontinuespecification-waitingresponse): 
    ResponseSpecification
```

## Properties<a name="aws-properties-lex-bot-waitandcontinuespecification-properties"></a>

`ContinueResponse`  <a name="cfn-lex-bot-waitandcontinuespecification-continueresponse"></a>
The response that Amazon Lex sends to indicate that the bot is ready to continue the conversation\.  
*Required*: Yes  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-waitandcontinuespecification-isactive"></a>
Specifies whether the bot will wait for a user to respond\. When this field is false, wait and continue responses for a slot aren't used\. If the `IsActive` field isn't specified, the default is true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StillWaitingResponse`  <a name="cfn-lex-bot-waitandcontinuespecification-stillwaitingresponse"></a>
A response that Amazon Lex sends periodically to the user to indicate that the bot is still waiting for input from the user\.  
*Required*: No  
*Type*: [StillWaitingResponseSpecification](aws-properties-lex-bot-stillwaitingresponsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitingResponse`  <a name="cfn-lex-bot-waitandcontinuespecification-waitingresponse"></a>
The response that Amazon Lex sends to indicate that the bot is waiting for the conversation to continue\.  
*Required*: Yes  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)