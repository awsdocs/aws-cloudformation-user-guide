# AWS::Lex::Bot PromptSpecification<a name="aws-properties-lex-bot-promptspecification"></a>

<a name="aws-properties-lex-bot-promptspecification-description"></a>The `PromptSpecification` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

## Syntax<a name="aws-properties-lex-bot-promptspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-promptspecification-syntax.json"></a>

```
{
  "[AllowInterrupt](#cfn-lex-bot-promptspecification-allowinterrupt)" : Boolean,
  "[MaxRetries](#cfn-lex-bot-promptspecification-maxretries)" : Integer,
  "[MessageGroupsList](#cfn-lex-bot-promptspecification-messagegroupslist)" : [ MessageGroup, ... ],
  "[MessageSelectionStrategy](#cfn-lex-bot-promptspecification-messageselectionstrategy)" : String,
  "[PromptAttemptsSpecification](#cfn-lex-bot-promptspecification-promptattemptsspecification)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-lex-bot-promptspecification-syntax.yaml"></a>

```
  [AllowInterrupt](#cfn-lex-bot-promptspecification-allowinterrupt): Boolean
  [MaxRetries](#cfn-lex-bot-promptspecification-maxretries): Integer
  [MessageGroupsList](#cfn-lex-bot-promptspecification-messagegroupslist): 
    - MessageGroup
  [MessageSelectionStrategy](#cfn-lex-bot-promptspecification-messageselectionstrategy): String
  [PromptAttemptsSpecification](#cfn-lex-bot-promptspecification-promptattemptsspecification): 
    Key : Value
```

## Properties<a name="aws-properties-lex-bot-promptspecification-properties"></a>

`AllowInterrupt`  <a name="cfn-lex-bot-promptspecification-allowinterrupt"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetries`  <a name="cfn-lex-bot-promptspecification-maxretries"></a>
Property description not available\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroupsList`  <a name="cfn-lex-bot-promptspecification-messagegroupslist"></a>
Property description not available\.  
*Required*: Yes  
*Type*: List of [MessageGroup](aws-properties-lex-bot-messagegroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageSelectionStrategy`  <a name="cfn-lex-bot-promptspecification-messageselectionstrategy"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromptAttemptsSpecification`  <a name="cfn-lex-bot-promptspecification-promptattemptsspecification"></a>
Specifies the advanced settings on each attempt of the prompt\. The valid keys are `Initial`, `Retry1`, `Retry2`, `Retry3`, `Retry4`, and `Retry5`\.  
*Required*: No  
*Type*: Map of [PromptAttemptSpecification](aws-properties-lex-bot-promptattemptspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)