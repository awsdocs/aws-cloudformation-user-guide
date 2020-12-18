# AWS::Cognito::UserPool StringAttributeConstraints<a name="aws-properties-cognito-userpool-stringattributeconstraints"></a>

The `StringAttributeConstraints` property type defines the string attribute constraints of an Amazon Cognito user pool\. `StringAttributeConstraints` is a subproperty of the [SchemaAttribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-userpool-schemaattribute.html) property type\.

## Syntax<a name="aws-properties-cognito-userpool-stringattributeconstraints-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-stringattributeconstraints-syntax.json"></a>

```
{
  "[MaxLength](#cfn-cognito-userpool-stringattributeconstraints-maxlength)" : String,
  "[MinLength](#cfn-cognito-userpool-stringattributeconstraints-minlength)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-stringattributeconstraints-syntax.yaml"></a>

```
  [MaxLength](#cfn-cognito-userpool-stringattributeconstraints-maxlength): String
  [MinLength](#cfn-cognito-userpool-stringattributeconstraints-minlength): String
```

## Properties<a name="aws-properties-cognito-userpool-stringattributeconstraints-properties"></a>

`MaxLength`  <a name="cfn-cognito-userpool-stringattributeconstraints-maxlength"></a>
The maximum length\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinLength`  <a name="cfn-cognito-userpool-stringattributeconstraints-minlength"></a>
The minimum length\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)