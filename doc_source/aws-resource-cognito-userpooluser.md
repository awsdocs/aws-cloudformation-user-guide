# AWS::Cognito::UserPoolUser<a name="aws-resource-cognito-userpooluser"></a>

The `AWS::Cognito::UserPoolUser` resource creates an Amazon Cognito user pool user\.

**Topics**
+ [Syntax](#aws-resource-cognito-userpooluser-syntax)
+ [Properties](#w3ab2c21c10d291b9)
+ [Return Value](#w3ab2c21c10d291c11)

## Syntax<a name="aws-resource-cognito-userpooluser-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpooluser-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolUser",
  "Properties" : {
  "[DesiredDeliveryMediums](#cfn-cognito-userpooluser-desireddeliverymediums)" : [ String, ... ],
  "[ForceAliasCreation](#cfn-cognito-userpooluser-forcealiascreation)" : Boolean,
  "[UserAttributes](#cfn-cognito-userpooluser-userattributes)" : [ AttributeType, ... ],
  "[MessageAction](#cfn-cognito-userpooluser-messageaction)" : String,
  "[Username](#cfn-cognito-userpooluser-username)" : String,
  "[UserPoolId](#cfn-cognito-userpooluser-userpoolid)" : String,
  "[ValidationData](#cfn-cognito-userpooluser-validationdata)" : [ AttributeType, ...]
  }
}
```

### YAML<a name="aws-resource-cognito-userpooluser-syntax.yaml"></a>

```
Type: "AWS::Cognito::UserPoolUser"
Properties:
  [DesiredDeliveryMediums](#cfn-cognito-userpooluser-desireddeliverymediums): 
    - String
  [ForceAliasCreation](#cfn-cognito-userpooluser-forcealiascreation): Boolean
  [UserAttributes](#cfn-cognito-userpooluser-userattributes): 
    - AttributeType
  [MessageAction](#cfn-cognito-userpooluser-messageaction): String
  [Username](#cfn-cognito-userpooluser-username): String
  [UserPoolId](#cfn-cognito-userpooluser-userpoolid): String
  [ValidationData](#cfn-cognito-userpooluser-validationdata): 
    - AttributeType
```

## Properties<a name="w3ab2c21c10d291b9"></a>

`DesiredDeliveryMediums`  <a name="cfn-cognito-userpooluser-desireddeliverymediums"></a>
Specifies how the welcome message will be sent\. For email, specify `EMAIL`\. To use a phone number, specify `SMS`\. You can specify more than one value\. The default value is `SMS`\.   
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ForceAliasCreation`  <a name="cfn-cognito-userpooluser-forcealiascreation"></a>
Use this parameter only if the `phone_number_verified` attribute or the `email_verified` attribute is set to `True`\. Otherwise, it is ignored\. The default value is `False`\.  
If this parameter is set to `True` and the phone number or email address specified in the `UserAttributes` parameter already exists as an alias with a different user, the API call migrates the alias from the previous user to the newly created user\. The previous user can no longer log in using that alias\.  
If this parameter is set to `False` and the alias already exists, the API throws an `AliasExistsException` error\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`UserAttributes`  <a name="cfn-cognito-userpooluser-userattributes"></a>
A list of name\-value pairs that contain user attributes and attribute values to be set for the user that you are creating\. You can create a user without specifying any attributes other than `Username`\. However, any attributes that you specify as required \(in `CreateUserPool` or in the **Attributes** tab of the console\) must be supplied either by you \(in your call to `AdminCreateUser`\) or by the user \(when signing up in response to your welcome message\)\.  
*Required*: No  
*Type*: List of [Amazon Cognito UserPoolUser AttributeType](aws-properties-cognito-userpooluser-attributetype.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MessageAction`  <a name="cfn-cognito-userpooluser-messageaction"></a>
Specifies the action you'd like to take for the message\. Valid values are `RESEND` and `SUPPRESS`\.  
To resend the invitation message to a user that already exists and reset the expiration limit on the user's account, set this parameter to `RESEND`\. To suppress sending the message, set it to `SUPPRESS`\. You can specify only one value\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Username`  <a name="cfn-cognito-userpooluser-username"></a>
The user name for the user\. `Username` must be unique within the user pool\. It must be a UTF\-8 string between 1 and 128 characters\. You can't change the username\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`UserPoolId`  <a name="cfn-cognito-userpooluser-userpoolid"></a>
The ID for the user pool where the user will be created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ValidationData`  <a name="cfn-cognito-userpooluser-validationdata"></a>
The user's validation data\. This is a list of name\-value pairs that contain user attributes and attribute values that you can use for custom validation, such as restricting the types of user accounts that can be registered\. For example, you might choose to allow or disallow user sign\-up based on the user's domain\.  
To configure custom validation, you must create a Pre Sign\-up Lambda trigger for the user pool\. The Lambda trigger receives the validation data and uses it in the validation process\. For more information, see [Customizing User Pool Workflows by Using AWS Lambda Triggers](http://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools-working-with-aws-lambda-triggers.html) in the *Amazon Cognito Developer Guide*\.  
*Required*: No  
*Type*: List of [Amazon Cognito UserPoolUser AttributeType](aws-properties-cognito-userpooluser-attributetype.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d291c11"></a>

### Ref<a name="w3ab2c21c10d291c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the name of the user\. For example, `admin`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.