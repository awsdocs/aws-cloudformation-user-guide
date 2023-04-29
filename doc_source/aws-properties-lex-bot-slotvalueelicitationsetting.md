# AWS::Lex::Bot SlotValueElicitationSetting<a name="aws-properties-lex-bot-slotvalueelicitationsetting"></a>

<a name="aws-properties-lex-bot-slotvalueelicitationsetting-description"></a>The `SlotValueElicitationSetting` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

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
Property description not available\.  
*Required*: No  
*Type*: [SlotDefaultValueSpecification](aws-properties-lex-bot-slotdefaultvaluespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromptSpecification`  <a name="cfn-lex-bot-slotvalueelicitationsetting-promptspecification"></a>
Property description not available\.  
*Required*: No  
*Type*: [PromptSpecification](aws-properties-lex-bot-promptspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampleUtterances`  <a name="cfn-lex-bot-slotvalueelicitationsetting-sampleutterances"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [SampleUtterance](aws-properties-lex-bot-sampleutterance.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotCaptureSetting`  <a name="cfn-lex-bot-slotvalueelicitationsetting-slotcapturesetting"></a>
Property description not available\.  
*Required*: No  
*Type*: [SlotCaptureSetting](aws-properties-lex-bot-slotcapturesetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotConstraint`  <a name="cfn-lex-bot-slotvalueelicitationsetting-slotconstraint"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitAndContinueSpecification`  <a name="cfn-lex-bot-slotvalueelicitationsetting-waitandcontinuespecification"></a>
Property description not available\.  
*Required*: No  
*Type*: [WaitAndContinueSpecification](aws-properties-lex-bot-waitandcontinuespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)