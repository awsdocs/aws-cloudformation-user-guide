# AWS::Lex::Bot PromptAttemptSpecification<a name="aws-properties-lex-bot-promptattemptspecification"></a>

Specifies the settings on a prompt attempt\.

## Syntax<a name="aws-properties-lex-bot-promptattemptspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-promptattemptspecification-syntax.json"></a>

```
{
  "[AllowedInputTypes](#cfn-lex-bot-promptattemptspecification-allowedinputtypes)" : AllowedInputTypes,
  "[AllowInterrupt](#cfn-lex-bot-promptattemptspecification-allowinterrupt)" : Boolean,
  "[AudioAndDTMFInputSpecification](#cfn-lex-bot-promptattemptspecification-audioanddtmfinputspecification)" : AudioAndDTMFInputSpecification,
  "[TextInputSpecification](#cfn-lex-bot-promptattemptspecification-textinputspecification)" : TextInputSpecification
}
```

### YAML<a name="aws-properties-lex-bot-promptattemptspecification-syntax.yaml"></a>

```
  [AllowedInputTypes](#cfn-lex-bot-promptattemptspecification-allowedinputtypes): 
    AllowedInputTypes
  [AllowInterrupt](#cfn-lex-bot-promptattemptspecification-allowinterrupt): Boolean
  [AudioAndDTMFInputSpecification](#cfn-lex-bot-promptattemptspecification-audioanddtmfinputspecification): 
    AudioAndDTMFInputSpecification
  [TextInputSpecification](#cfn-lex-bot-promptattemptspecification-textinputspecification): 
    TextInputSpecification
```

## Properties<a name="aws-properties-lex-bot-promptattemptspecification-properties"></a>

`AllowedInputTypes`  <a name="cfn-lex-bot-promptattemptspecification-allowedinputtypes"></a>
Indicates the allowed input types of the prompt attempt\.  
*Required*: Yes  
*Type*: [AllowedInputTypes](aws-properties-lex-bot-allowedinputtypes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowInterrupt`  <a name="cfn-lex-bot-promptattemptspecification-allowinterrupt"></a>
Indicates whether the user can interrupt a speech prompt attempt from the bot\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioAndDTMFInputSpecification`  <a name="cfn-lex-bot-promptattemptspecification-audioanddtmfinputspecification"></a>
Specifies the settings on audio and DTMF input\.  
*Required*: No  
*Type*: [AudioAndDTMFInputSpecification](aws-properties-lex-bot-audioanddtmfinputspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextInputSpecification`  <a name="cfn-lex-bot-promptattemptspecification-textinputspecification"></a>
Specifies the settings on text input\.  
*Required*: No  
*Type*: [TextInputSpecification](aws-properties-lex-bot-textinputspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)