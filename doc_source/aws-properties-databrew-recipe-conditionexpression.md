# AWS::DataBrew::Recipe ConditionExpression<a name="aws-properties-databrew-recipe-conditionexpression"></a>

Represents an individual condition that evaluates to true or false\.

Conditions are used with recipe actions: The action is only performed for column values where the condition evaluates to true\.

If a recipe requires more than one condition, then the recipe must specify multiple `ConditionExpression` elements\. Each condition is applied to the rows in a dataset first, before the recipe action is performed\.

## Syntax<a name="aws-properties-databrew-recipe-conditionexpression-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-recipe-conditionexpression-syntax.json"></a>

```
{
  "[Condition](#cfn-databrew-recipe-conditionexpression-condition)" : String,
  "[TargetColumn](#cfn-databrew-recipe-conditionexpression-targetcolumn)" : String,
  "[Value](#cfn-databrew-recipe-conditionexpression-value)" : String
}
```

### YAML<a name="aws-properties-databrew-recipe-conditionexpression-syntax.yaml"></a>

```
  [Condition](#cfn-databrew-recipe-conditionexpression-condition): String
  [TargetColumn](#cfn-databrew-recipe-conditionexpression-targetcolumn): String
  [Value](#cfn-databrew-recipe-conditionexpression-value): String
```

## Properties<a name="aws-properties-databrew-recipe-conditionexpression-properties"></a>

`Condition`  <a name="cfn-databrew-recipe-conditionexpression-condition"></a>
A specific condition to apply to a recipe action\. For more information, see [Recipe structure](https://docs.aws.amazon.com/databrew/latest/dg/recipe-structure.html) in the *AWS Glue DataBrew Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[A-Z\_]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetColumn`  <a name="cfn-databrew-recipe-conditionexpression-targetcolumn"></a>
A column to apply this condition to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-databrew-recipe-conditionexpression-value"></a>
A value that the condition must evaluate to for the condition to succeed\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)