# AWS::Lex::Bot ConditionalSpecification<a name="aws-properties-lex-bot-conditionalspecification"></a>

Provides a list of conditional branches\. Branches are evaluated in the order that they are entered in the list\. The first branch with a condition that evaluates to true is executed\. The last branch in the list is the default branch\. The default branch should not have any condition expression\. The default branch is executed if no other branch has a matching condition\.

## Syntax<a name="aws-properties-lex-bot-conditionalspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-conditionalspecification-syntax.json"></a>

```
{
  "[ConditionalBranches](#cfn-lex-bot-conditionalspecification-conditionalbranches)" : [ ConditionalBranch, ... ],
  "[DefaultBranch](#cfn-lex-bot-conditionalspecification-defaultbranch)" : DefaultConditionalBranch,
  "[IsActive](#cfn-lex-bot-conditionalspecification-isactive)" : Boolean
}
```

### YAML<a name="aws-properties-lex-bot-conditionalspecification-syntax.yaml"></a>

```
  [ConditionalBranches](#cfn-lex-bot-conditionalspecification-conditionalbranches): 
    - ConditionalBranch
  [DefaultBranch](#cfn-lex-bot-conditionalspecification-defaultbranch): 
    DefaultConditionalBranch
  [IsActive](#cfn-lex-bot-conditionalspecification-isactive): Boolean
```

## Properties<a name="aws-properties-lex-bot-conditionalspecification-properties"></a>

`ConditionalBranches`  <a name="cfn-lex-bot-conditionalspecification-conditionalbranches"></a>
A list of conditional branches\. A conditional branch is made up of a condition, a response and a next step\. The response and next step are executed when the condition is true\.  
*Required*: Yes  
*Type*: List of [ConditionalBranch](aws-properties-lex-bot-conditionalbranch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultBranch`  <a name="cfn-lex-bot-conditionalspecification-defaultbranch"></a>
The conditional branch that should be followed when the conditions for other branches are not satisfied\. A conditional branch is made up of a condition, a response and a next step\.  
*Required*: Yes  
*Type*: [DefaultConditionalBranch](aws-properties-lex-bot-defaultconditionalbranch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-conditionalspecification-isactive"></a>
Determines whether a conditional branch is active\. When `IsActive` is false, the conditions are not evaluated\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)