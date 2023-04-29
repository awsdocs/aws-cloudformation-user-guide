# AWS::Lex::Bot ConditionalSpecification<a name="aws-properties-lex-bot-conditionalspecification"></a>

<a name="aws-properties-lex-bot-conditionalspecification-description"></a>The `ConditionalSpecification` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

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
Property description not available\.  
*Required*: Yes  
*Type*: List of [ConditionalBranch](aws-properties-lex-bot-conditionalbranch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultBranch`  <a name="cfn-lex-bot-conditionalspecification-defaultbranch"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [DefaultConditionalBranch](aws-properties-lex-bot-defaultconditionalbranch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-conditionalspecification-isactive"></a>
Determines whether a conditional branch is active\. When `IsActive` is false, the conditions are not evaluated\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)