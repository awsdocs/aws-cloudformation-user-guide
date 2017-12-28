# Amazon Cognito UserPool SchemaAttribute<a name="aws-properties-cognito-userpool-schemaattribute"></a>

`SchemaAttribute` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the schema attributes of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-schemaattribute-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-schemaattribute-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-attributedatatype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-developeronlyattribute)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-mutable)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-numberattributeconstraints)" : NumberAttributeConstraintsType,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-stringattributeconstraints)" : StringAttributeConstraintsType,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-required)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpool-schemaattribute-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-attributedatatype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-developeronlyattribute): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-mutable): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-numberattributeconstraints):
  NumberAttributeConstraints
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-stringattributeconstraints):
  StringAttributeConstraints
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-schemaattribute-required): Boolean
```

## Properties<a name="aws-properties-cognito-userpool-schemaattribute-properties"></a>

`AttributeDataType`  
The attribute data type\. Can be one of the following: `String`, `Number`, `DateTime`, or `Boolean`\.  
*Type*: String  
*Required: *No

`DeveloperOnlyAttribute`  
Specifies whether the attribute type is developer only\.  
*Type*: Boolean  
*Required: *No

`Mutable`  
Specifies whether the attribute can be changed after it has been created\. `True` means mutable and `False` means immutable\.  
*Type*: Boolean  
*Required: *No

`Name`  
A schema attribute of the name type\.  
*Type*: String  
*Required: *No

`NumberAttributeConstraints`  
Specifies the constraints for an attribute of the number type\.  
*Type*: [Amazon Cognito UserPool NumberAttributeConstraints](aws-properties-cognito-userpool-numberattributeconstraints.md)  
*Required: *No

`StringAttributeConstraints`  
Specifies the constraints for an attribute of the string type\.  
*Type*: [Amazon Cognito UserPool StringAttributeConstraints](aws-properties-cognito-userpool-stringattributeconstraints.md)  
*Required: *No

`Required`  
Specifies whether a user pool attribute is required\. If the attribute is required and the user does not provide a value, registration or sign\-in fails\.  
*Type*: Boolean  
*Required: *No