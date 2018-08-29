# Amazon Cognito UserPool StringAttributeConstraints<a name="aws-properties-cognito-userpool-stringattributeconstraints"></a>

The `StringAttributeConstraints` property type defines the string attribute constraints of an Amazon Cognito User Pool\. `StringAttributeConstraints` is a subproperty of the [Amazon Cognito UserPool SchemaAttribute](aws-properties-cognito-userpool-schemaattribute.md) property type\.

## Syntax<a name="aws-properties-cognito-userpool-stringattributeconstraints-syntax"></a>

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
The maximum value of an attribute that is of the string data type\.  
*Type*: String  
*Required*: No

`MinLength`  <a name="cfn-cognito-userpool-stringattributeconstraints-minlength"></a>
The minimum value of an attribute that is of the string data type\.  
*Type*: String  
*Required*: No