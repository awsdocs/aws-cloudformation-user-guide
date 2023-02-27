# AWS::Lex::Bot ConditionalBranch<a name="aws-properties-lex-bot-conditionalbranch"></a>

A set of actions that Amazon Lex should run if the condition is matched\.

## Syntax<a name="aws-properties-lex-bot-conditionalbranch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-conditionalbranch-syntax.json"></a>

```
{
  "[Condition](#cfn-lex-bot-conditionalbranch-condition)" : Condition,
  "[Name](#cfn-lex-bot-conditionalbranch-name)" : String,
  "[NextStep](#cfn-lex-bot-conditionalbranch-nextstep)" : DialogState,
  "[Response](#cfn-lex-bot-conditionalbranch-response)" : ResponseSpecification
}
```

### YAML<a name="aws-properties-lex-bot-conditionalbranch-syntax.yaml"></a>

```
  [Condition](#cfn-lex-bot-conditionalbranch-condition): 
    Condition
  [Name](#cfn-lex-bot-conditionalbranch-name): String
  [NextStep](#cfn-lex-bot-conditionalbranch-nextstep): 
    DialogState
  [Response](#cfn-lex-bot-conditionalbranch-response): 
    ResponseSpecification
```

## Properties<a name="aws-properties-lex-bot-conditionalbranch-properties"></a>

`Condition`  <a name="cfn-lex-bot-conditionalbranch-condition"></a>
Contains the expression to evaluate\. If the condition is true, the branch's actions are taken\.  
*Required*: Yes  
*Type*: [Condition](aws-properties-lex-bot-condition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lex-bot-conditionalbranch-name"></a>
The name of the branch\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextStep`  <a name="cfn-lex-bot-conditionalbranch-nextstep"></a>
The next step in the conversation\.  
*Required*: Yes  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Response`  <a name="cfn-lex-bot-conditionalbranch-response"></a>
Specifies a list of message groups that Amazon Lex uses to respond the user input\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)