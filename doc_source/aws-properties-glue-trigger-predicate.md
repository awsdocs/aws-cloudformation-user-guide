# AWS Glue Trigger Predicate<a name="aws-properties-glue-trigger-predicate"></a>

<a name="aws-properties-glue-trigger-predicate-description"></a>The `Predicate` property type specifies the predicate of an AWS Glue job trigger, which determines when it fires\.

<a name="aws-properties-glue-trigger-predicate-inheritance"></a> `Predicate` is a property of the [AWS::Glue::Trigger](aws-resource-glue-trigger.md) resource\.

## Syntax<a name="aws-properties-glue-trigger-predicate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-trigger-predicate-syntax.json"></a>

```
{
  "[Logical](#cfn-glue-trigger-predicate-logical)" : String,
  "[Conditions](#cfn-glue-trigger-predicate-conditions)" : [ [*Condition*](aws-properties-glue-trigger-condition.md), ... ]
}
```

### YAML<a name="aws-properties-glue-trigger-predicate-syntax.yaml"></a>

```
[Logical](#cfn-glue-trigger-predicate-logical): String
[Conditions](#cfn-glue-trigger-predicate-conditions): 
  - [*Condition*](aws-properties-glue-trigger-condition.md)
```

## Properties<a name="aws-properties-glue-trigger-predicate-properties"></a>

`Logical`  <a name="cfn-glue-trigger-predicate-logical"></a>
The logical operator for the predicate\.  
*Valid values*: `AND`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Conditions`  <a name="cfn-glue-trigger-predicate-conditions"></a>
The conditions that determine when the trigger fires\.  
 *Required*: No  
 *Type*: List of [AWS Glue Trigger Condition](aws-properties-glue-trigger-condition.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-trigger-predicate-seealso"></a>
+ [ Predicate Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Predicate) in the *AWS Glue Developer Guide*