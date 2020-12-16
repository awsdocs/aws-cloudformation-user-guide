# AWS::DataBrew::Recipe RecipeStep<a name="aws-properties-databrew-recipe-recipestep"></a>

Represents a single step from a DataBrew recipe to be performed\.

## Syntax<a name="aws-properties-databrew-recipe-recipestep-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-recipe-recipestep-syntax.json"></a>

```
{
  "[Action](#cfn-databrew-recipe-recipestep-action)" : Action,
  "[ConditionExpressions](#cfn-databrew-recipe-recipestep-conditionexpressions)" : [ ConditionExpression, ... ]
}
```

### YAML<a name="aws-properties-databrew-recipe-recipestep-syntax.yaml"></a>

```
  [Action](#cfn-databrew-recipe-recipestep-action): 
    Action
  [ConditionExpressions](#cfn-databrew-recipe-recipestep-conditionexpressions): 
    - ConditionExpression
```

## Properties<a name="aws-properties-databrew-recipe-recipestep-properties"></a>

`Action`  <a name="cfn-databrew-recipe-recipestep-action"></a>
The particular action to be performed in the recipe step\.  
*Required*: Yes  
*Type*: [Action](aws-properties-databrew-recipe-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConditionExpressions`  <a name="cfn-databrew-recipe-recipestep-conditionexpressions"></a>
One or more conditions that must be met, in order for the recipe step to succeed\.  
All of the conditions in the array must be met\. In other words, all of the conditions must be combined using a logical AND operation\.
*Required*: No  
*Type*: List of [ConditionExpression](aws-properties-databrew-recipe-conditionexpression.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)