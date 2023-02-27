# AWS::Lex::Bot Intent<a name="aws-properties-lex-bot-intent"></a>

Represents an action that the user wants to perform\.

## Syntax<a name="aws-properties-lex-bot-intent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-intent-syntax.json"></a>

```
{
  "[Description](#cfn-lex-bot-intent-description)" : String,
  "[DialogCodeHook](#cfn-lex-bot-intent-dialogcodehook)" : DialogCodeHookSetting,
  "[FulfillmentCodeHook](#cfn-lex-bot-intent-fulfillmentcodehook)" : FulfillmentCodeHookSetting,
  "[InitialResponseSetting](#cfn-lex-bot-intent-initialresponsesetting)" : InitialResponseSetting,
  "[InputContexts](#cfn-lex-bot-intent-inputcontexts)" : [ InputContext, ... ],
  "[IntentClosingSetting](#cfn-lex-bot-intent-intentclosingsetting)" : IntentClosingSetting,
  "[IntentConfirmationSetting](#cfn-lex-bot-intent-intentconfirmationsetting)" : IntentConfirmationSetting,
  "[KendraConfiguration](#cfn-lex-bot-intent-kendraconfiguration)" : KendraConfiguration,
  "[Name](#cfn-lex-bot-intent-name)" : String,
  "[OutputContexts](#cfn-lex-bot-intent-outputcontexts)" : [ OutputContext, ... ],
  "[ParentIntentSignature](#cfn-lex-bot-intent-parentintentsignature)" : String,
  "[SampleUtterances](#cfn-lex-bot-intent-sampleutterances)" : [ SampleUtterance, ... ],
  "[SlotPriorities](#cfn-lex-bot-intent-slotpriorities)" : [ SlotPriority, ... ],
  "[Slots](#cfn-lex-bot-intent-slots)" : [ Slot, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-intent-syntax.yaml"></a>

```
  [Description](#cfn-lex-bot-intent-description): String
  [DialogCodeHook](#cfn-lex-bot-intent-dialogcodehook): 
    DialogCodeHookSetting
  [FulfillmentCodeHook](#cfn-lex-bot-intent-fulfillmentcodehook): 
    FulfillmentCodeHookSetting
  [InitialResponseSetting](#cfn-lex-bot-intent-initialresponsesetting): 
    InitialResponseSetting
  [InputContexts](#cfn-lex-bot-intent-inputcontexts): 
    - InputContext
  [IntentClosingSetting](#cfn-lex-bot-intent-intentclosingsetting): 
    IntentClosingSetting
  [IntentConfirmationSetting](#cfn-lex-bot-intent-intentconfirmationsetting): 
    IntentConfirmationSetting
  [KendraConfiguration](#cfn-lex-bot-intent-kendraconfiguration): 
    KendraConfiguration
  [Name](#cfn-lex-bot-intent-name): String
  [OutputContexts](#cfn-lex-bot-intent-outputcontexts): 
    - OutputContext
  [ParentIntentSignature](#cfn-lex-bot-intent-parentintentsignature): String
  [SampleUtterances](#cfn-lex-bot-intent-sampleutterances): 
    - SampleUtterance
  [SlotPriorities](#cfn-lex-bot-intent-slotpriorities): 
    - SlotPriority
  [Slots](#cfn-lex-bot-intent-slots): 
    - Slot
```

## Properties<a name="aws-properties-lex-bot-intent-properties"></a>

`Description`  <a name="cfn-lex-bot-intent-description"></a>
A description of the intent\. Use the description to help identify the intent in lists\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DialogCodeHook`  <a name="cfn-lex-bot-intent-dialogcodehook"></a>
Specifies that Amazon Lex invokes the alias Lambda function for each user input\. You can invoke this Lambda function to personalize user interaction\.  
*Required*: No  
*Type*: [DialogCodeHookSetting](aws-properties-lex-bot-dialogcodehooksetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FulfillmentCodeHook`  <a name="cfn-lex-bot-intent-fulfillmentcodehook"></a>
Specifies that Amazon Lex invokes the alias Lambda function when the intent is ready for fulfillment\. You can invoke this function to complete the bot's transaction with the user\.  
*Required*: No  
*Type*: [FulfillmentCodeHookSetting](aws-properties-lex-bot-fulfillmentcodehooksetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InitialResponseSetting`  <a name="cfn-lex-bot-intent-initialresponsesetting"></a>
Configuration setting for a response sent to the user before Amazon Lex starts eliciting slots\.  
*Required*: No  
*Type*: [InitialResponseSetting](aws-properties-lex-bot-initialresponsesetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputContexts`  <a name="cfn-lex-bot-intent-inputcontexts"></a>
A list of contexts that must be active for this intent to be considered by Amazon Lex\.  
*Required*: No  
*Type*: List of [InputContext](aws-properties-lex-bot-inputcontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntentClosingSetting`  <a name="cfn-lex-bot-intent-intentclosingsetting"></a>
Sets the response that Amazon Lex sends to the user when the intent is closed\.  
*Required*: No  
*Type*: [IntentClosingSetting](aws-properties-lex-bot-intentclosingsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntentConfirmationSetting`  <a name="cfn-lex-bot-intent-intentconfirmationsetting"></a>
Provides prompts that Amazon Lex sends to the user to confirm the completion of an intent\. If the user answers "no," the settings contain a statement that is sent to the user to end the intent\.  
*Required*: No  
*Type*: [IntentConfirmationSetting](aws-properties-lex-bot-intentconfirmationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KendraConfiguration`  <a name="cfn-lex-bot-intent-kendraconfiguration"></a>
Provides configuration information for the `AMAZON.KendraSearchIntent` intent\. When you use this intent, Amazon Lex searches the specified Amazon Kendra index and returns documents from the index that match the user's utterance\.  
*Required*: No  
*Type*: [KendraConfiguration](aws-properties-lex-bot-kendraconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lex-bot-intent-name"></a>
The name of the intent\. Intent names must be unique within the locale that contains the intent and can't match the name of any built\-in intent\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputContexts`  <a name="cfn-lex-bot-intent-outputcontexts"></a>
A list of contexts that the intent activates when it is fulfilled\.  
*Required*: No  
*Type*: List of [OutputContext](aws-properties-lex-bot-outputcontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParentIntentSignature`  <a name="cfn-lex-bot-intent-parentintentsignature"></a>
A unique identifier for the built\-in intent to base this intent on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampleUtterances`  <a name="cfn-lex-bot-intent-sampleutterances"></a>
A list of utterances that a user might say to signal the intent\.  
*Required*: No  
*Type*: List of [SampleUtterance](aws-properties-lex-bot-sampleutterance.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotPriorities`  <a name="cfn-lex-bot-intent-slotpriorities"></a>
Indicates the priority for slots\. Amazon Lex prompts the user for slot values in priority order\.  
*Required*: No  
*Type*: List of [SlotPriority](aws-properties-lex-bot-slotpriority.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slots`  <a name="cfn-lex-bot-intent-slots"></a>
A list of slots that the intent requires for fulfillment\.  
*Required*: No  
*Type*: List of [Slot](aws-properties-lex-bot-slot.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)