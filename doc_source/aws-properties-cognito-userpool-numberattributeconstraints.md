# Amazon Cognito UserPool NumberAttributeConstraints<a name="aws-properties-cognito-userpool-numberattributeconstraints"></a>

The `NumberAttributeConstraints` property type defines the number attribute constraints of an Amazon Cognito User Pool\. `NumberAttributeConstraints` is a subproperty of the [Amazon Cognito UserPool SchemaAttribute](aws-properties-cognito-userpool-schemaattribute.md) property type\.

## Syntax<a name="aws-properties-cognito-userpool-numberattributeconstraints-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-numberattributeconstraints-syntax.json"></a>

```
{
  "[MaxValue](#cfn-cognito-userpool-numberattributeconstraints-maxvalue)" : String,
  "[MinValue](#cfn-cognito-userpool-numberattributeconstraints-minvalue)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-numberattributeconstraints-syntax.yaml"></a>

```
[MaxValue](#cfn-cognito-userpool-numberattributeconstraints-maxvalue): String
[MinValue](#cfn-cognito-userpool-numberattributeconstraints-minvalue): String
```

## Properties<a name="aws-properties-cognito-userpool-numberattributeconstraints-properties"></a>

`MaxValue`  <a name="cfn-cognito-userpool-numberattributeconstraints-maxvalue"></a>
The maximum value of an attribute that is of the number data type\.  
*Type*: String  
*Required*: No

`MinValue`  <a name="cfn-cognito-userpool-numberattributeconstraints-minvalue"></a>
The minimum value of an attribute that is of the number data type\.  
*Type*: String  
*Required*: No