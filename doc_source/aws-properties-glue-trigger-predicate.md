# AWS::Glue::Trigger Predicate<a name="aws-properties-glue-trigger-predicate"></a>

Defines the predicate of the trigger, which determines when it fires\.

## Syntax<a name="aws-properties-glue-trigger-predicate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-trigger-predicate-syntax.json"></a>

```
{
  "[Conditions](#cfn-glue-trigger-predicate-conditions)" : [ Condition, ... ],
  "[Logical](#cfn-glue-trigger-predicate-logical)" : String
}
```

### YAML<a name="aws-properties-glue-trigger-predicate-syntax.yaml"></a>

```
  [Conditions](#cfn-glue-trigger-predicate-conditions): 
    - Condition
  [Logical](#cfn-glue-trigger-predicate-logical): String
```

## Properties<a name="aws-properties-glue-trigger-predicate-properties"></a>

`Conditions`  <a name="cfn-glue-trigger-predicate-conditions"></a>
A list of the conditions that determine when the trigger will fire\.  
*Required*: No  
*Type*: List of [Condition](aws-properties-glue-trigger-condition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logical`  <a name="cfn-glue-trigger-predicate-logical"></a>
An optional field if only one condition is listed\. If multiple conditions are listed, then this field is required\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-glue-trigger-predicate--seealso"></a>
+  [Predicate Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Predicate) in the *AWS Glue Developer Guide* 

