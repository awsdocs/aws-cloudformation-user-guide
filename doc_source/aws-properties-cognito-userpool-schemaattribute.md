# Amazon Cognito UserPool SchemaAttribute<a name="aws-properties-cognito-userpool-schemaattribute"></a>

`SchemaAttribute` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the schema attributes of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-schemaattribute-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-schemaattribute-syntax.json"></a>

```
{
  "[AttributeDataType](#cfn-cognito-userpool-schemaattribute-attributedatatype)" : String,
  "[DeveloperOnlyAttribute](#cfn-cognito-userpool-schemaattribute-developeronlyattribute)" : Boolean,
  "[Mutable](#cfn-cognito-userpool-schemaattribute-mutable)" : Boolean,
  "[Name](#cfn-cognito-userpool-schemaattribute-name)" : String,
  "[NumberAttributeConstraints](#cfn-cognito-userpool-schemaattribute-numberattributeconstraints)" : NumberAttributeConstraintsType,
  "[StringAttributeConstraints](#cfn-cognito-userpool-schemaattribute-stringattributeconstraints)" : StringAttributeConstraintsType,
  "[Required](#cfn-cognito-userpool-schemaattribute-required)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpool-schemaattribute-syntax.yaml"></a>

```
[AttributeDataType](#cfn-cognito-userpool-schemaattribute-attributedatatype): String
[DeveloperOnlyAttribute](#cfn-cognito-userpool-schemaattribute-developeronlyattribute): Boolean
[Mutable](#cfn-cognito-userpool-schemaattribute-mutable): Boolean
[Name](#cfn-cognito-userpool-schemaattribute-name): String
[NumberAttributeConstraints](#cfn-cognito-userpool-schemaattribute-numberattributeconstraints):
  NumberAttributeConstraints
[StringAttributeConstraints](#cfn-cognito-userpool-schemaattribute-stringattributeconstraints):
  StringAttributeConstraints
[Required](#cfn-cognito-userpool-schemaattribute-required): Boolean
```

## Properties<a name="aws-properties-cognito-userpool-schemaattribute-properties"></a>

`AttributeDataType`  <a name="cfn-cognito-userpool-schemaattribute-attributedatatype"></a>
The attribute data type\. Can be one of the following: `String`, `Number`, `DateTime`, or `Boolean`\.  
*Type*: String  
*Required*: No

`DeveloperOnlyAttribute`  <a name="cfn-cognito-userpool-schemaattribute-developeronlyattribute"></a>
Specifies whether the attribute type is developer only\.  
*Type*: Boolean  
*Required*: No

`Mutable`  <a name="cfn-cognito-userpool-schemaattribute-mutable"></a>
Specifies whether the attribute can be changed after it has been created\. `True` means mutable and `False` means immutable\.  
*Type*: Boolean  
*Required*: No

`Name`  <a name="cfn-cognito-userpool-schemaattribute-name"></a>
A schema attribute of the name type\.  
*Type*: String  
*Required*: No

`NumberAttributeConstraints`  <a name="cfn-cognito-userpool-schemaattribute-numberattributeconstraints"></a>
Specifies the constraints for an attribute of the number type\.  
*Type*: [Amazon Cognito UserPool NumberAttributeConstraints](aws-properties-cognito-userpool-numberattributeconstraints.md)  
*Required*: No

`StringAttributeConstraints`  <a name="cfn-cognito-userpool-schemaattribute-stringattributeconstraints"></a>
Specifies the constraints for an attribute of the string type\.  
*Type*: [Amazon Cognito UserPool StringAttributeConstraints](aws-properties-cognito-userpool-stringattributeconstraints.md)  
*Required*: No

`Required`  <a name="cfn-cognito-userpool-schemaattribute-required"></a>
Specifies whether a user pool attribute is required\. If the attribute is required and the user does not provide a value, registration or sign\-in fails\.  
*Type*: Boolean  
*Required*: No