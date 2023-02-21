# AWS::Lex::Bot ElicitationCodeHookInvocationSetting<a name="aws-properties-lex-bot-elicitationcodehookinvocationsetting"></a>

Settings that specify the dialog code hook that is called by Amazon Lex between eliciting slot values\.

## Syntax<a name="aws-properties-lex-bot-elicitationcodehookinvocationsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-elicitationcodehookinvocationsetting-syntax.json"></a>

```
{
  "[EnableCodeHookInvocation](#cfn-lex-bot-elicitationcodehookinvocationsetting-enablecodehookinvocation)" : Boolean,
  "[InvocationLabel](#cfn-lex-bot-elicitationcodehookinvocationsetting-invocationlabel)" : String
}
```

### YAML<a name="aws-properties-lex-bot-elicitationcodehookinvocationsetting-syntax.yaml"></a>

```
  [EnableCodeHookInvocation](#cfn-lex-bot-elicitationcodehookinvocationsetting-enablecodehookinvocation): Boolean
  [InvocationLabel](#cfn-lex-bot-elicitationcodehookinvocationsetting-invocationlabel): String
```

## Properties<a name="aws-properties-lex-bot-elicitationcodehookinvocationsetting-properties"></a>

`EnableCodeHookInvocation`  <a name="cfn-lex-bot-elicitationcodehookinvocationsetting-enablecodehookinvocation"></a>
Indicates whether a Lambda function should be invoked for the dialog\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationLabel`  <a name="cfn-lex-bot-elicitationcodehookinvocationsetting-invocationlabel"></a>
A label that indicates the dialog step from which the dialog code hook is happening\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)