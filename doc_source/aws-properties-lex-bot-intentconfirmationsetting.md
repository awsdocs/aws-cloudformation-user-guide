# AWS::Lex::Bot IntentConfirmationSetting<a name="aws-properties-lex-bot-intentconfirmationsetting"></a>

Provides a prompt for making sure that the user is ready for the intent to be fulfilled\.

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
The `DialogCodeHookInvocationSetting` object associated with intent's confirmation step\. The dialog code hook is triggered based on these invocation settings when the confirmation next step or declination next step or failure next step is `InvokeDialogCodeHook`\.   
*Required*: No  
*Type*: [DialogCodeHookInvocationSetting](aws-properties-lex-bot-dialogcodehookinvocationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfirmationConditional`  <a name="cfn-lex-bot-intentconfirmationsetting-confirmationconditional"></a>
A list of conditional branches to evaluate after the intent is closed\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfirmationNextStep`  <a name="cfn-lex-bot-intentconfirmationsetting-confirmationnextstep"></a>
Specifies the next step that the bot executes when the customer confirms the intent\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfirmationResponse`  <a name="cfn-lex-bot-intentconfirmationsetting-confirmationresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond the user input\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeclinationConditional`  <a name="cfn-lex-bot-intentconfirmationsetting-declinationconditional"></a>
A list of conditional branches to evaluate after the intent is declined\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeclinationNextStep`  <a name="cfn-lex-bot-intentconfirmationsetting-declinationnextstep"></a>
Specifies the next step that the bot executes when the customer declines the intent\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeclinationResponse`  <a name="cfn-lex-bot-intentconfirmationsetting-declinationresponse"></a>
When the user answers "no" to the question defined in `promptSpecification`, Amazon Lex responds with this response to acknowledge that the intent was canceled\.   
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElicitationCodeHook`  <a name="cfn-lex-bot-intentconfirmationsetting-elicitationcodehook"></a>
The `DialogCodeHookInvocationSetting` used when the code hook is invoked during confirmation prompt retries\.  
*Required*: No  
*Type*: [ElicitationCodeHookInvocationSetting](aws-properties-lex-bot-elicitationcodehookinvocationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureConditional`  <a name="cfn-lex-bot-intentconfirmationsetting-failureconditional"></a>
Provides a list of conditional branches\. Branches are evaluated in the order that they are entered in the list\. The first branch with a condition that evaluates to true is executed\. The last branch in the list is the default branch\. The default branch should not have any condition expression\. The default branch is executed if no other branch has a matching condition\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureNextStep`  <a name="cfn-lex-bot-intentconfirmationsetting-failurenextstep"></a>
The next step to take in the conversation if the confirmation step fails\.  
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
Prompts the user to confirm the intent\. This question should have a yes or no answer\.  
Amazon Lex uses this prompt to ensure that the user acknowledges that the intent is ready for fulfillment\. For example, with the `OrderPizza` intent, you might want to confirm that the order is correct before placing it\. For other intents, such as intents that simply respond to user questions, you might not need to ask the user for confirmation before providing the information\.   
*Required*: Yes  
*Type*: [PromptSpecification](aws-properties-lex-bot-promptspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)