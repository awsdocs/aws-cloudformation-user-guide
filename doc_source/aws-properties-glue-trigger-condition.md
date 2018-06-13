# AWS Glue Trigger Condition<a name="aws-properties-glue-trigger-condition"></a>

<a name="aws-properties-glue-trigger-condition-description"></a>The `Condition` property type specifies a condition for an AWS Glue job trigger predicate\.

<a name="aws-properties-glue-trigger-condition-inheritance"></a> The `Conditions` property of the [AWS Glue Trigger Predicate](aws-properties-glue-trigger-predicate.md) property type contains a list of `Condition` property types\.

## Syntax<a name="aws-properties-glue-trigger-condition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-trigger-condition-syntax.json"></a>

```
{
  "[LogicalOperator](#cfn-glue-trigger-condition-logicaloperator)" : String,
  "[JobName](#cfn-glue-trigger-condition-jobname)" : String,
  "[State](#cfn-glue-trigger-condition-state)" : String
}
```

### YAML<a name="aws-properties-glue-trigger-condition-syntax.yaml"></a>

```
[LogicalOperator](#cfn-glue-trigger-condition-logicaloperator): String
[JobName](#cfn-glue-trigger-condition-jobname): String
[State](#cfn-glue-trigger-condition-state): String
```

## Properties<a name="aws-properties-glue-trigger-condition-properties"></a>

`LogicalOperator`  <a name="cfn-glue-trigger-condition-logicaloperator"></a>
The logical operator for the condition\.  
*Valid values*: `EQUALS`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`JobName`  <a name="cfn-glue-trigger-condition-jobname"></a>
The name of the associated job\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`State`  <a name="cfn-glue-trigger-condition-state"></a>
The state of the condition\.  
*Valid values*: `SUCCEEDED`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-trigger-condition-seealso"></a>
+ [ Condition Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Condition) in the *AWS Glue Developer Guide*