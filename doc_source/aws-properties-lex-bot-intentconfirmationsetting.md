# AWS::Lex::Bot IntentConfirmationSetting<a name="aws-properties-lex-bot-intentconfirmationsetting"></a>

<a name="aws-properties-lex-bot-intentconfirmationsetting-description"></a>The `IntentConfirmationSetting` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

## Syntax<a name="aws-properties-lex-bot-intentconfirmationsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-intentconfirmationsetting-syntax.json"></a>

```
{
  "[CodeHook](#cfn-lex-bot-intentconfirmationsetting-codehook)" : DialogCodeHookInvocationSetting,
  "[ConfirmationConditional](#cfn-lex-bot-intentconfirmationsetting-confirmationconditional)" : ConditionalSpecification,
  "[ConfirmationNextStep](#cfn-lex-bot-intentconfirmationsetting-confirmationnextstep)" : DialogState,
  "[ConfirmationResponse](#cfn-lex-bot-intentconfirmationsetting-confirmationresponse)" : ResponseSpecification,
  "[DeclinationConditional](#cfn-lex-bot-intentconfirmationsetting-declinationconditional)" : ConditionalSpecification,
  "[DeclinationNextStep](#cfn-lex-bot-intentconfirmationsetting-declinationnextstep)" : DialogState,
  "[DeclinationResponse](#cfn-lex-bot-intentconfirmationsetting-declinationresponse)" : ResponseSpecification,
  "[ElicitationCodeHook](#cfn-lex-bot-intentconfirmationsetting-elicitationcodehook)" : ElicitationCodeHookInvocationSetting,
  "[FailureConditional](#cfn-lex-bot-intentconfirmationsetting-failureconditional)" : ConditionalSpecification,
  "[FailureNextStep](#cfn-lex-bot-intentconfirmationsetting-failurenextstep)" : DialogState,
  "[FailureResponse](#cfn-lex-bot-intentconfirmationsetting-failureresponse)" : ResponseSpecification,
  "[IsActive](#cfn-lex-bot-intentconfirmationsetting-isactive)" : Boolean,
  "[PromptSpecification](#cfn-lex-bot-intentconfirmationsetting-promptspecification)" : PromptSpecification
}
```

### YAML<a name="aws-properties-lex-bot-intentconfirmationsetting-syntax.yaml"></a>

```
  [CodeHook](#cfn-lex-bot-intentconfirmationsetting-codehook): 
    DialogCodeHookInvocationSetting
  [ConfirmationConditional](#cfn-lex-bot-intentconfirmationsetting-confirmationconditional): 
    ConditionalSpecification
  [ConfirmationNextStep](#cfn-lex-bot-intentconfirmationsetting-confirmationnextstep): 
    DialogState
  [ConfirmationResponse](#cfn-lex-bot-intentconfirmationsetting-confirmationresponse): 
    ResponseSpecification
  [DeclinationConditional](#cfn-lex-bot-intentconfirmationsetting-declinationconditional): 
    ConditionalSpecification
  [DeclinationNextStep](#cfn-lex-bot-intentconfirmationsetting-declinationnextstep): 
    DialogState
  [DeclinationResponse](#cfn-lex-bot-intentconfirmationsetting-declinationresponse): 
    ResponseSpecification
  [ElicitationCodeHook](#cfn-lex-bot-intentconfirmationsetting-elicitationcodehook): 
    ElicitationCodeHookInvocationSetting
  [FailureConditional](#cfn-lex-bot-intentconfirmationsetting-failureconditional): 
    ConditionalSpecification
  [FailureNextStep](#cfn-lex-bot-intentconfirmationsetting-failurenextstep): 
    DialogState
  [FailureResponse](#cfn-lex-bot-intentconfirmationsetting-failureresponse): 
    ResponseSpecification
  [IsActive](#cfn-lex-bot-intentconfirmationsetting-isactive): Boolean
  [PromptSpecification](#cfn-lex-bot-intentconfirmationsetting-promptspecification): 
    PromptSpecification
```

## Properties<a name="aws-properties-lex-bot-intentconfirmationsetting-properties"></a>

`CodeHook`  <a name="cfn-lex-bot-intentconfirmationsetting-codehook"></a>
Property description not available\.  
*Required*: No  
*Type*: [DialogCodeHookInvocationSetting](aws-properties-lex-bot-dialogcodehookinvocationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfirmationConditional`  <a name="cfn-lex-bot-intentconfirmationsetting-confirmationconditional"></a>
Property description not available\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfirmationNextStep`  <a name="cfn-lex-bot-intentconfirmationsetting-confirmationnextstep"></a>
Property description not available\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfirmationResponse`  <a name="cfn-lex-bot-intentconfirmationsetting-confirmationresponse"></a>
Property description not available\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeclinationConditional`  <a name="cfn-lex-bot-intentconfirmationsetting-declinationconditional"></a>
Property description not available\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeclinationNextStep`  <a name="cfn-lex-bot-intentconfirmationsetting-declinationnextstep"></a>
Property description not available\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeclinationResponse`  <a name="cfn-lex-bot-intentconfirmationsetting-declinationresponse"></a>
Property description not available\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElicitationCodeHook`  <a name="cfn-lex-bot-intentconfirmationsetting-elicitationcodehook"></a>
Property description not available\.  
*Required*: No  
*Type*: [ElicitationCodeHookInvocationSetting](aws-properties-lex-bot-elicitationcodehookinvocationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureConditional`  <a name="cfn-lex-bot-intentconfirmationsetting-failureconditional"></a>
Property description not available\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureNextStep`  <a name="cfn-lex-bot-intentconfirmationsetting-failurenextstep"></a>
Property description not available\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureResponse`  <a name="cfn-lex-bot-intentconfirmationsetting-failureresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond the user input when the intent confirmation fails\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-intentconfirmationsetting-isactive"></a>
Specifies whether the intent's confirmation is sent to the user\. When this field is false, confirmation and declination responses aren't sent\. If the `IsActive` field isn't specified, the default is true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromptSpecification`  <a name="cfn-lex-bot-intentconfirmationsetting-promptspecification"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [PromptSpecification](aws-properties-lex-bot-promptspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)