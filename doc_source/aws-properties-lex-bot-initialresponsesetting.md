# AWS::Lex::Bot InitialResponseSetting<a name="aws-properties-lex-bot-initialresponsesetting"></a>

<a name="aws-properties-lex-bot-initialresponsesetting-description"></a>The `InitialResponseSetting` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

## Syntax<a name="aws-properties-lex-bot-initialresponsesetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-initialresponsesetting-syntax.json"></a>

```
{
  "[CodeHook](#cfn-lex-bot-initialresponsesetting-codehook)" : DialogCodeHookInvocationSetting,
  "[Conditional](#cfn-lex-bot-initialresponsesetting-conditional)" : ConditionalSpecification,
  "[InitialResponse](#cfn-lex-bot-initialresponsesetting-initialresponse)" : ResponseSpecification,
  "[NextStep](#cfn-lex-bot-initialresponsesetting-nextstep)" : DialogState
}
```

### YAML<a name="aws-properties-lex-bot-initialresponsesetting-syntax.yaml"></a>

```
  [CodeHook](#cfn-lex-bot-initialresponsesetting-codehook): 
    DialogCodeHookInvocationSetting
  [Conditional](#cfn-lex-bot-initialresponsesetting-conditional): 
    ConditionalSpecification
  [InitialResponse](#cfn-lex-bot-initialresponsesetting-initialresponse): 
    ResponseSpecification
  [NextStep](#cfn-lex-bot-initialresponsesetting-nextstep): 
    DialogState
```

## Properties<a name="aws-properties-lex-bot-initialresponsesetting-properties"></a>

`CodeHook`  <a name="cfn-lex-bot-initialresponsesetting-codehook"></a>
Property description not available\.  
*Required*: No  
*Type*: [DialogCodeHookInvocationSetting](aws-properties-lex-bot-dialogcodehookinvocationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Conditional`  <a name="cfn-lex-bot-initialresponsesetting-conditional"></a>
Property description not available\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InitialResponse`  <a name="cfn-lex-bot-initialresponsesetting-initialresponse"></a>
Property description not available\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextStep`  <a name="cfn-lex-bot-initialresponsesetting-nextstep"></a>
Property description not available\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)