# AWS::Lex::Bot SlotValueElicitationSetting<a name="aws-properties-lex-bot-slotvalueelicitationsetting"></a>

Specifies the elicitation setting details eliciting a slot\.

## Syntax<a name="aws-properties-lex-bot-slotvalueelicitationsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotvalueelicitationsetting-syntax.json"></a>

```
{
  "[DefaultValueSpecification](#cfn-lex-bot-slotvalueelicitationsetting-defaultvaluespecification)" : SlotDefaultValueSpecification,
  "[PromptSpecification](#cfn-lex-bot-slotvalueelicitationsetting-promptspecification)" : PromptSpecification,
  "[SampleUtterances](#cfn-lex-bot-slotvalueelicitationsetting-sampleutterances)" : [ SampleUtterance, ... ],
  "[SlotCaptureSetting](#cfn-lex-bot-slotvalueelicitationsetting-slotcapturesetting)" : SlotCaptureSetting,
  "[SlotConstraint](#cfn-lex-bot-slotvalueelicitationsetting-slotconstraint)" : String,
  "[WaitAndContinueSpecification](#cfn-lex-bot-slotvalueelicitationsetting-waitandcontinuespecification)" : WaitAndContinueSpecification
}
```

### YAML<a name="aws-properties-lex-bot-slotvalueelicitationsetting-syntax.yaml"></a>

```
  [DefaultValueSpecification](#cfn-lex-bot-slotvalueelicitationsetting-defaultvaluespecification): 
    SlotDefaultValueSpecification
  [PromptSpecification](#cfn-lex-bot-slotvalueelicitationsetting-promptspecification): 
    PromptSpecification
  [SampleUtterances](#cfn-lex-bot-slotvalueelicitationsetting-sampleutterances): 
    - SampleUtterance
  [SlotCaptureSetting](#cfn-lex-bot-slotvalueelicitationsetting-slotcapturesetting): 
    SlotCaptureSetting
  [SlotConstraint](#cfn-lex-bot-slotvalueelicitationsetting-slotconstraint): String
  [WaitAndContinueSpecification](#cfn-lex-bot-slotvalueelicitationsetting-waitandcontinuespecification): 
    WaitAndContinueSpecification
```

## Properties<a name="aws-properties-lex-bot-slotvalueelicitationsetting-properties"></a>

`DefaultValueSpecification`  <a name="cfn-lex-bot-slotvalueelicitationsetting-defaultvaluespecification"></a>
A list of default values for a slot\. Default values are used when Amazon Lex hasn't determined a value for a slot\. You can specify default values from context variables, session attributes, and defined values\.  
*Required*: No  
*Type*: [SlotDefaultValueSpecification](aws-properties-lex-bot-slotdefaultvaluespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromptSpecification`  <a name="cfn-lex-bot-slotvalueelicitationsetting-promptspecification"></a>
The prompt that Amazon Lex uses to elicit the slot value from the user\.  
*Required*: No  
*Type*: [PromptSpecification](aws-properties-lex-bot-promptspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampleUtterances`  <a name="cfn-lex-bot-slotvalueelicitationsetting-sampleutterances"></a>
If you know a specific pattern that users might respond to an Amazon Lex request for a slot value, you can provide those utterances to improve accuracy\. This is optional\. In most cases, Amazon Lex is capable of understanding user utterances\.  
*Required*: No  
*Type*: List of [SampleUtterance](aws-properties-lex-bot-sampleutterance.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotCaptureSetting`  <a name="cfn-lex-bot-slotvalueelicitationsetting-slotcapturesetting"></a>
Specifies the settings that Amazon Lex uses when a slot value is successfully entered by a user\.  
*Required*: No  
*Type*: [SlotCaptureSetting](aws-properties-lex-bot-slotcapturesetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotConstraint`  <a name="cfn-lex-bot-slotvalueelicitationsetting-slotconstraint"></a>
Specifies whether the slot is required or optional\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitAndContinueSpecification`  <a name="cfn-lex-bot-slotvalueelicitationsetting-waitandcontinuespecification"></a>
Specifies the prompts that Amazon Lex uses while a bot is waiting for customer input\.   
*Required*: No  
*Type*: [WaitAndContinueSpecification](aws-properties-lex-bot-waitandcontinuespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)