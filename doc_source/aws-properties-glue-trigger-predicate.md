# AWS Glue Trigger Predicate<a name="aws-properties-glue-trigger-predicate"></a>

<a name="aws-properties-glue-trigger-predicate-description"></a>The `Predicate` property type specifies the predicate of an AWS Glue job trigger, which determines when it fires\.

<a name="aws-properties-glue-trigger-predicate-inheritance"></a> `Predicate` is a property of the [AWS::Glue::Trigger](aws-resource-glue-trigger.md) resource\.

## Syntax<a name="aws-properties-glue-trigger-predicate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-trigger-predicate-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-trigger-predicate-logical)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-trigger-predicate-conditions)" : [ Condition, ... ]
}
```

### YAML<a name="aws-properties-glue-trigger-predicate-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-trigger-predicate-logical): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-trigger-predicate-conditions): 
  - Condition
```

## Properties<a name="aws-properties-glue-trigger-predicate-properties"></a>

`Logical`  
The logical operator for the predicate\.  
*Valid values*: `AND`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Conditions`  
The conditions that determine when the trigger fires\.  
 *Required*: No  
 *Type*: List of   
 *Update requires*: No interruption 

## See Also<a name="aws-properties-glue-trigger-predicate-seealso"></a>

+ [ Predicate Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Predicate) in the *AWS Glue Developer Guide*