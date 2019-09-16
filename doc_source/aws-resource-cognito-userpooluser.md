# AWS::Cognito::UserPoolUser<a name="aws-resource-cognito-userpooluser"></a>

The `AWS::Cognito::UserPoolUser` resource creates an Amazon Cognito user pool user\.

## Syntax<a name="aws-resource-cognito-userpooluser-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpooluser-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolUser",
  "Properties" : {
      "[DesiredDeliveryMediums](#cfn-cognito-userpooluser-desireddeliverymediums)" : [ String, ... ],
      "[ForceAliasCreation](#cfn-cognito-userpooluser-forcealiascreation)" : Boolean,
      "[MessageAction](#cfn-cognito-userpooluser-messageaction)" : String,
      "[UserAttributes](#cfn-cognito-userpooluser-userattributes)" : [ [AttributeType](aws-properties-cognito-userpooluser-attributetype.md), ... ],
      "[UserPoolId](#cfn-cognito-userpooluser-userpoolid)" : String,
      "[Username](#cfn-cognito-userpooluser-username)" : String,
      "[ValidationData](#cfn-cognito-userpooluser-validationdata)" : [ [AttributeType](aws-properties-cognito-userpooluser-attributetype.md), ... ]
    }
}
```

### YAML<a name="aws-resource-cognito-userpooluser-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolUser
Properties: 
  [DesiredDeliveryMediums](#cfn-cognito-userpooluser-desireddeliverymediums): 
    - String
  [ForceAliasCreation](#cfn-cognito-userpooluser-forcealiascreation): Boolean
  [MessageAction](#cfn-cognito-userpooluser-messageaction): String
  [UserAttributes](#cfn-cognito-userpooluser-userattributes): 
    - [AttributeType](aws-properties-cognito-userpooluser-attributetype.md)
  [UserPoolId](#cfn-cognito-userpooluser-userpoolid): String
  [Username](#cfn-cognito-userpooluser-username): String
  [ValidationData](#cfn-cognito-userpooluser-validationdata): 
    - [AttributeType](aws-properties-cognito-userpooluser-attributetype.md)
```

## Properties<a name="aws-resource-cognito-userpooluser-properties"></a>

`DesiredDeliveryMediums`  <a name="cfn-cognito-userpooluser-desireddeliverymediums"></a>
Specify `"EMAIL"` if email will be used to send the welcome message\. Specify `"SMS"` if the phone number will be used\. The default value is `"SMS"`\. More than one value can be specified\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ForceAliasCreation`  <a name="cfn-cognito-userpooluser-forcealiascreation"></a>
This parameter is only used if the `phone_number_verified` or `email_verified` attribute is set to `True`\. Otherwise, it is ignored\.  
If this parameter is set to `True` and the phone number or email address specified in the UserAttributes parameter already exists as an alias with a different user, the API call will migrate the alias from the previous user to the newly created user\. The previous user will no longer be able to log in using that alias\.  
If this parameter is set to `False`, the API throws an `AliasExistsException` error if the alias already exists\. The default value is `False`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MessageAction`  <a name="cfn-cognito-userpooluser-messageaction"></a>
Set to `"RESEND"` to resend the invitation message to a user that already exists and reset the expiration limit on the user's account\. Set to `"SUPPRESS"` to suppress sending the message\. Only one value can be specified\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `RESEND | SUPPRESS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserAttributes`  <a name="cfn-cognito-userpooluser-userattributes"></a>
An array of name\-value pairs that contain user attributes and attribute values to be set for the user to be created\. You can create a user without specifying any attributes other than `Username`\. However, any attributes that you specify as required \(in [https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_CreateUserPool.html](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_CreateUserPool.html) or in the **Attributes** tab of the console\) must be supplied either by you \(in your call to `AdminCreateUser`\) or by the user \(when he or she signs up in response to your welcome message\)\.  
For custom attributes, you must prepend the `custom:` prefix to the attribute name\.  
To send a message inviting the user to sign up, you must specify the user's email address or phone number\. This can be done in your call to AdminCreateUser or in the **Users** tab of the Amazon Cognito console for managing your user pools\.  
In your call to `AdminCreateUser`, you can set the `email_verified` attribute to `True`, and you can set the `phone_number_verified` attribute to `True`\. \(You can also do this by calling [https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_AdminUpdateUserAttributes.html](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_AdminUpdateUserAttributes.html)\.\)  
+  **email**: The email address of the user to whom the message that contains the code and username will be sent\. Required if the `email_verified` attribute is set to `True`, or if `"EMAIL"` is specified in the `DesiredDeliveryMediums` parameter\.
+  **phone\_number**: The phone number of the user to whom the message that contains the code and username will be sent\. Required if the `phone_number_verified` attribute is set to `True`, or if `"SMS"` is specified in the `DesiredDeliveryMediums` parameter\.
*Required*: No  
*Type*: List of [AttributeType](aws-properties-cognito-userpooluser-attributetype.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserPoolId`  <a name="cfn-cognito-userpooluser-userpoolid"></a>
The user pool ID for the user pool where the user will be created\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Username`  <a name="cfn-cognito-userpooluser-username"></a>
The username for the user\. Must be unique within the user pool\. Must be a UTF\-8 string between 1 and 128 characters\. After the user is created, the username cannot be changed\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidationData`  <a name="cfn-cognito-userpooluser-validationdata"></a>
The user's validation data\. This is an array of name\-value pairs that contain user attributes and attribute values that you can use for custom validation, such as restricting the types of user accounts that can be registered\. For example, you might choose to allow or disallow user sign\-up based on the user's domain\.  
To configure custom validation, you must create a Pre Sign\-up Lambda trigger for the user pool as described in the Amazon Cognito Developer Guide\. The Lambda trigger receives the validation data and uses it in the validation process\.  
The user's validation data is not persisted\.  
*Required*: No  
*Type*: List of [AttributeType](aws-properties-cognito-userpooluser-attributetype.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-cognito-userpooluser-return-values"></a>

### Ref<a name="aws-resource-cognito-userpooluser-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the user\. For example, `admin`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.