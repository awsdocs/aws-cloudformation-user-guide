# AWS::Lex::Bot DefaultConditionalBranch<a name="aws-properties-lex-bot-defaultconditionalbranch"></a>

A set of actions that Amazon Lex should run if none of the other conditions are met\.

## Syntax<a name="aws-properties-lex-bot-defaultconditionalbranch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-defaultconditionalbranch-syntax.json"></a>

```
{
  "[NextStep](#cfn-lex-bot-defaultconditionalbranch-nextstep)" : DialogState,
  "[Response](#cfn-lex-bot-defaultconditionalbranch-response)" : ResponseSpecification
}
```

### YAML<a name="aws-properties-lex-bot-defaultconditionalbranch-syntax.yaml"></a>

```
  [NextStep](#cfn-lex-bot-defaultconditionalbranch-nextstep): 
    DialogState
  [Response](#cfn-lex-bot-defaultconditionalbranch-response): 
    ResponseSpecification
```

## Properties<a name="aws-properties-lex-bot-defaultconditionalbranch-properties"></a>

`NextStep`  <a name="cfn-lex-bot-defaultconditionalbranch-nextstep"></a>
The next step in the conversation\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Response`  <a name="cfn-lex-bot-defaultconditionalbranch-response"></a>
Specifies a list of message groups that Amazon Lex uses to respond the user input\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)