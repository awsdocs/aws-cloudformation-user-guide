# AWS::Lex::Bot SlotCaptureSetting<a name="aws-properties-lex-bot-slotcapturesetting"></a>

Settings used when Amazon Lex successfully captures a slot value from a user\.

## Syntax<a name="aws-properties-lex-bot-slotcapturesetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotcapturesetting-syntax.json"></a>

```
{
  "[CaptureConditional](#cfn-lex-bot-slotcapturesetting-captureconditional)" : ConditionalSpecification,
  "[CaptureNextStep](#cfn-lex-bot-slotcapturesetting-capturenextstep)" : DialogState,
  "[CaptureResponse](#cfn-lex-bot-slotcapturesetting-captureresponse)" : ResponseSpecification,
  "[CodeHook](#cfn-lex-bot-slotcapturesetting-codehook)" : DialogCodeHookInvocationSetting,
  "[ElicitationCodeHook](#cfn-lex-bot-slotcapturesetting-elicitationcodehook)" : ElicitationCodeHookInvocationSetting,
  "[FailureConditional](#cfn-lex-bot-slotcapturesetting-failureconditional)" : ConditionalSpecification,
  "[FailureNextStep](#cfn-lex-bot-slotcapturesetting-failurenextstep)" : DialogState,
  "[FailureResponse](#cfn-lex-bot-slotcapturesetting-failureresponse)" : ResponseSpecification
}
```

### YAML<a name="aws-properties-lex-bot-slotcapturesetting-syntax.yaml"></a>

```
  [CaptureConditional](#cfn-lex-bot-slotcapturesetting-captureconditional): 
    ConditionalSpecification
  [CaptureNextStep](#cfn-lex-bot-slotcapturesetting-capturenextstep): 
    DialogState
  [CaptureResponse](#cfn-lex-bot-slotcapturesetting-captureresponse): 
    ResponseSpecification
  [CodeHook](#cfn-lex-bot-slotcapturesetting-codehook): 
    DialogCodeHookInvocationSetting
  [ElicitationCodeHook](#cfn-lex-bot-slotcapturesetting-elicitationcodehook): 
    ElicitationCodeHookInvocationSetting
  [FailureConditional](#cfn-lex-bot-slotcapturesetting-failureconditional): 
    ConditionalSpecification
  [FailureNextStep](#cfn-lex-bot-slotcapturesetting-failurenextstep): 
    DialogState
  [FailureResponse](#cfn-lex-bot-slotcapturesetting-failureresponse): 
    ResponseSpecification
```

## Properties<a name="aws-properties-lex-bot-slotcapturesetting-properties"></a>

`CaptureConditional`  <a name="cfn-lex-bot-slotcapturesetting-captureconditional"></a>
A list of conditional branches to evaluate after the slot value is captured\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptureNextStep`  <a name="cfn-lex-bot-slotcapturesetting-capturenextstep"></a>
Specifies the next step that the bot runs when the slot value is captured before the code hook times out\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptureResponse`  <a name="cfn-lex-bot-slotcapturesetting-captureresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond the user input\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodeHook`  <a name="cfn-lex-bot-slotcapturesetting-codehook"></a>
Code hook called after Amazon Lex successfully captures a slot value\.  
*Required*: No  
*Type*: [DialogCodeHookInvocationSetting](aws-properties-lex-bot-dialogcodehookinvocationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElicitationCodeHook`  <a name="cfn-lex-bot-slotcapturesetting-elicitationcodehook"></a>
Code hook called when Amazon Lex doesn't capture a slot value\.  
*Required*: No  
*Type*: [ElicitationCodeHookInvocationSetting](aws-properties-lex-bot-elicitationcodehookinvocationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureConditional`  <a name="cfn-lex-bot-slotcapturesetting-failureconditional"></a>
A list of conditional branches to evaluate when the slot value isn't captured\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureNextStep`  <a name="cfn-lex-bot-slotcapturesetting-failurenextstep"></a>
Specifies the next step that the bot runs when the slot value code is not recognized\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureResponse`  <a name="cfn-lex-bot-slotcapturesetting-failureresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond the user input when the slot fails to be captured\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)