# AWS::Lex::Bot PostDialogCodeHookInvocationSpecification<a name="aws-properties-lex-bot-postdialogcodehookinvocationspecification"></a>

Specifies next steps to run after the dialog code hook finishes\.

## Syntax<a name="aws-properties-lex-bot-postdialogcodehookinvocationspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-postdialogcodehookinvocationspecification-syntax.json"></a>

```
{
  "[FailureConditional](#cfn-lex-bot-postdialogcodehookinvocationspecification-failureconditional)" : ConditionalSpecification,
  "[FailureNextStep](#cfn-lex-bot-postdialogcodehookinvocationspecification-failurenextstep)" : DialogState,
  "[FailureResponse](#cfn-lex-bot-postdialogcodehookinvocationspecification-failureresponse)" : ResponseSpecification,
  "[SuccessConditional](#cfn-lex-bot-postdialogcodehookinvocationspecification-successconditional)" : ConditionalSpecification,
  "[SuccessNextStep](#cfn-lex-bot-postdialogcodehookinvocationspecification-successnextstep)" : DialogState,
  "[SuccessResponse](#cfn-lex-bot-postdialogcodehookinvocationspecification-successresponse)" : ResponseSpecification,
  "[TimeoutConditional](#cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutconditional)" : ConditionalSpecification,
  "[TimeoutNextStep](#cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutnextstep)" : DialogState,
  "[TimeoutResponse](#cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutresponse)" : ResponseSpecification
}
```

### YAML<a name="aws-properties-lex-bot-postdialogcodehookinvocationspecification-syntax.yaml"></a>

```
  [FailureConditional](#cfn-lex-bot-postdialogcodehookinvocationspecification-failureconditional): 
    ConditionalSpecification
  [FailureNextStep](#cfn-lex-bot-postdialogcodehookinvocationspecification-failurenextstep): 
    DialogState
  [FailureResponse](#cfn-lex-bot-postdialogcodehookinvocationspecification-failureresponse): 
    ResponseSpecification
  [SuccessConditional](#cfn-lex-bot-postdialogcodehookinvocationspecification-successconditional): 
    ConditionalSpecification
  [SuccessNextStep](#cfn-lex-bot-postdialogcodehookinvocationspecification-successnextstep): 
    DialogState
  [SuccessResponse](#cfn-lex-bot-postdialogcodehookinvocationspecification-successresponse): 
    ResponseSpecification
  [TimeoutConditional](#cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutconditional): 
    ConditionalSpecification
  [TimeoutNextStep](#cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutnextstep): 
    DialogState
  [TimeoutResponse](#cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutresponse): 
    ResponseSpecification
```

## Properties<a name="aws-properties-lex-bot-postdialogcodehookinvocationspecification-properties"></a>

`FailureConditional`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-failureconditional"></a>
A list of conditional branches to evaluate after the dialog code hook throws an exception or returns with the `State` field of the `Intent` object set to `Failed`\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureNextStep`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-failurenextstep"></a>
Specifies the next step the bot runs after the dialog code hook throws an exception or returns with the `State` field of the `Intent` object set to `Failed`\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureResponse`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-failureresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond the user input when the code hook fails\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessConditional`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-successconditional"></a>
A list of conditional branches to evaluate after the dialog code hook finishes successfully\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessNextStep`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-successnextstep"></a>
Specifics the next step the bot runs after the dialog code hook finishes successfully\.   
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessResponse`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-successresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond when the code hook succeeds\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutConditional`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutconditional"></a>
A list of conditional branches to evaluate if the code hook times out\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutNextStep`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutnextstep"></a>
Specifies the next step that the bot runs when the code hook times out\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutResponse`  <a name="cfn-lex-bot-postdialogcodehookinvocationspecification-timeoutresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond to the user input when the code hook times out\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)