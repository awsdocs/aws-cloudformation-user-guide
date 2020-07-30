# AWS::Cognito::UserPool SchemaAttribute<a name="aws-properties-cognito-userpool-schemaattribute"></a>

Contains information about the schema attribute\.

## Syntax<a name="aws-properties-cognito-userpool-schemaattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-schemaattribute-syntax.json"></a>

```
{
  "[AttributeDataType](#cfn-cognito-userpool-schemaattribute-attributedatatype)" : String,
  "[DeveloperOnlyAttribute](#cfn-cognito-userpool-schemaattribute-developeronlyattribute)" : Boolean,
  "[Mutable](#cfn-cognito-userpool-schemaattribute-mutable)" : Boolean,
  "[Name](#cfn-cognito-userpool-schemaattribute-name)" : String,
  "[NumberAttributeConstraints](#cfn-cognito-userpool-schemaattribute-numberattributeconstraints)" : NumberAttributeConstraints,
  "[Required](#cfn-cognito-userpool-schemaattribute-required)" : Boolean,
  "[StringAttributeConstraints](#cfn-cognito-userpool-schemaattribute-stringattributeconstraints)" : StringAttributeConstraints
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
  [Required](#cfn-cognito-userpool-schemaattribute-required): Boolean
  [StringAttributeConstraints](#cfn-cognito-userpool-schemaattribute-stringattributeconstraints): 
    StringAttributeConstraints
```

## Properties<a name="aws-properties-cognito-userpool-schemaattribute-properties"></a>

`AttributeDataType`  <a name="cfn-cognito-userpool-schemaattribute-attributedatatype"></a>
The attribute data type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Boolean | DateTime | Number | String`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeveloperOnlyAttribute`  <a name="cfn-cognito-userpool-schemaattribute-developeronlyattribute"></a>
We recommend that you use [WriteAttributes](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_UserPoolClientType.html#CognitoUserPools-Type-UserPoolClientType-WriteAttributes) in the user pool client to control how attributes can be mutated for new use cases instead of using `DeveloperOnlyAttribute`\.
Specifies whether the attribute type is developer only\. This attribute can only be modified by an administrator\. Users will not be able to modify this attribute using their access token\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mutable`  <a name="cfn-cognito-userpool-schemaattribute-mutable"></a>
Specifies whether the value of the attribute can be changed\.  
For any user pool attribute that's mapped to an identity provider attribute, you must set this parameter to `true`\. Amazon Cognito updates mapped attributes when users sign in to your application through an identity provider\. If an attribute is immutable, Amazon Cognito throws an error when it attempts to update the attribute\. For more information, see [Specifying Identity Provider Attribute Mappings for Your User Pool](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools-specifying-attribute-mapping.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cognito-userpool-schemaattribute-name"></a>
A schema attribute of the name type\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `20`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberAttributeConstraints`  <a name="cfn-cognito-userpool-schemaattribute-numberattributeconstraints"></a>
Specifies the constraints for an attribute of the number type\.  
*Required*: No  
*Type*: [NumberAttributeConstraints](aws-properties-cognito-userpool-numberattributeconstraints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Required`  <a name="cfn-cognito-userpool-schemaattribute-required"></a>
Specifies whether a user pool attribute is required\. If the attribute is required and the user does not provide a value, registration or sign\-in will fail\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringAttributeConstraints`  <a name="cfn-cognito-userpool-schemaattribute-stringattributeconstraints"></a>
Specifies the constraints for an attribute of the string type\.  
*Required*: No  
*Type*: [StringAttributeConstraints](aws-properties-cognito-userpool-stringattributeconstraints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)