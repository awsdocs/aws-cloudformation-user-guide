# AWS Glue Trigger Action<a name="aws-properties-glue-trigger-action"></a>

<a name="aws-properties-glue-trigger-action-description"></a>The `Action` property type specifies the actions that an AWS Glue job trigger initiates when it fires\.

<a name="aws-properties-glue-trigger-action-inheritance"></a> `Action` is a property of the [AWS::Glue::Trigger](aws-resource-glue-trigger.md) resource\.

## Syntax<a name="aws-properties-glue-trigger-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-trigger-action-syntax.json"></a>

```
{
  "[JobName](#cfn-glue-trigger-action-jobname)" : String,
  "[Arguments](#cfn-glue-trigger-action-arguments)" : JSON object
}
```

### YAML<a name="aws-properties-glue-trigger-action-syntax.yaml"></a>

```
[JobName](#cfn-glue-trigger-action-jobname): String
[Arguments](#cfn-glue-trigger-action-arguments): JSON object
```

## Properties<a name="aws-properties-glue-trigger-action-properties"></a>

`JobName`  <a name="cfn-glue-trigger-action-jobname"></a>
The name of the associated job\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Arguments`  <a name="cfn-glue-trigger-action-arguments"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the arguments for the action\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-trigger-action-seealso"></a>
+ [ Action Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Action) in the *AWS Glue Developer Guide*