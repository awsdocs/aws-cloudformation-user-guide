# AWS::Cognito::UserPool<a name="aws-resource-cognito-userpool"></a>

The `AWS::Cognito::UserPool` resource creates an Amazon Cognito user pool\. For more information on working with Amazon Cognito user pools, see [Amazon Cognito User Pools](http://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html) and [CreateUserPool](http://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_CreateUserPool.html)\.

**Topics**
+ [Syntax](#aws-resource-cognito-userpool-syntax)
+ [Properties](#w3ab2c21c10d279b9)
+ [Return Value](#w3ab2c21c10d279c11)

## Syntax<a name="aws-resource-cognito-userpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpool-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPool",
  "Properties" : {
    "[AdminCreateUserConfig](#cfn-cognito-userpool-admincreateuserconfig)" : AdminCreateUserConfig,
    "[AliasAttributes](#cfn-cognito-userpool-aliasattributes)" : [ String ],
    "[AutoVerifiedAttributes](#cfn-cognito-userpool-autoverifiedattributes)" : [ String ],
    "[DeviceConfiguration](#cfn-cognito-userpool-deviceconfiguration)" : DeviceConfiguration,
    "[EmailConfiguration](#cfn-cognito-userpool-emailconfiguration)" : EmailConfiguration,
    "[EmailVerificationMessage](#cfn-cognito-userpool-emailverificationmessage)" : String,
    "[EmailVerificationSubject](#cfn-cognito-userpool-emailverificationsubject)" : String,
    "[LambdaConfig](#cfn-cognito-userpool-lambdaconfig)" : LambdaConfig,
    "[MfaConfiguration](#cfn-cognito-userpool-mfaconfiguration)" : String,
    "[Policies](#cfn-cognito-userpool-policies)" : Policies,
    "[UserPoolName](#cfn-cognito-userpool-poolname)" : String,
    "[Schema](#cfn-cognito-userpool-schema)" : [ [*SchemaAttribute*](aws-properties-cognito-userpool-schemaattribute.md) ],
    "[SmsAuthenticationMessage](#cfn-cognito-userpool-smsauthenticationmessage)" : String,
    "[SmsConfiguration](#cfn-cognito-userpool-smsconfiguration)" : SmsConfiguration,
    "[SmsVerificationMessage](#cfn-cognito-userpool-smsverificationmessage)" : String,
    "[UserPoolTags](#cfn-cognito-userpool-userpooltags)" : { String:String, ... }
  }
}
```

### YAML<a name="aws-resource-cognito-userpool-syntax.yaml"></a>

```
Type: "AWS::Cognito::UserPool"
Properties:
  [AdminCreateUserConfig](#cfn-cognito-userpool-admincreateuserconfig): 
    AdminCreateUserConfig
  [AliasAttributes](#cfn-cognito-userpool-aliasattributes): 
    - String
  [AutoVerifiedAttributes](#cfn-cognito-userpool-autoverifiedattributes): 
    - String
  [DeviceConfiguration](#cfn-cognito-userpool-deviceconfiguration): 
    DeviceConfiguration
  [EmailConfiguration](#cfn-cognito-userpool-emailconfiguration): 
    EmailConfiguration
  [EmailVerificationMessage](#cfn-cognito-userpool-emailverificationmessage): String
  [EmailVerificationSubject](#cfn-cognito-userpool-emailverificationsubject): String
  [LambdaConfig](#cfn-cognito-userpool-lambdaconfig): 
    LambdaConfig
  [MfaConfiguration](#cfn-cognito-userpool-mfaconfiguration): String
  [Policies](#cfn-cognito-userpool-policies): 
    Policies
  [UserPoolName](#cfn-cognito-userpool-poolname): String
  [Schema](#cfn-cognito-userpool-schema): 
    - [*SchemaAttribute*](aws-properties-cognito-userpool-schemaattribute.md)
  [SmsAuthenticationMessage](#cfn-cognito-userpool-smsauthenticationmessage): String
  [SmsConfiguration](#cfn-cognito-userpool-smsconfiguration): 
    SmsConfiguration
  [SmsVerificationMessage](#cfn-cognito-userpool-smsverificationmessage): String
  [UserPoolTags](#cfn-cognito-userpool-userpooltags): 
    String: String
```

## Properties<a name="w3ab2c21c10d279b9"></a>

`AdminCreateUserConfig`  <a name="cfn-cognito-userpool-admincreateuserconfig"></a>
The type of configuration for creating a new user profile\.  
*Required*: No  
*Type*: [Amazon Cognito UserPool AdminCreateUserConfig](aws-properties-cognito-userpool-admincreateuserconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AliasAttributes`  <a name="cfn-cognito-userpool-aliasattributes"></a>
Attributes supported as an alias for this user pool\. Possible values: `phone_number`, `email`, and/or `preferred_username`\.   
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutoVerifiedAttributes`  <a name="cfn-cognito-userpool-autoverifiedattributes"></a>
The attributes to be auto\-verified\. Possible values: `email` and/or `phone_number`\.   
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DeviceConfiguration`  <a name="cfn-cognito-userpool-deviceconfiguration"></a>
The type of configuration for the user pool's device tracking\.  
*Required*: No  
*Type*: [Amazon Cognito UserPool DeviceConfiguration](aws-properties-cognito-userpool-deviceconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EmailConfiguration`  <a name="cfn-cognito-userpool-emailconfiguration"></a>
The email configuration\.  
*Required*: No  
*Type*: [Amazon Cognito UserPool EmailConfiguration](aws-properties-cognito-userpool-emailconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EmailVerificationMessage`  <a name="cfn-cognito-userpool-emailverificationmessage"></a>
A string representing the email verification message\. Must contain `{####}` in the description\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EmailVerificationSubject`  <a name="cfn-cognito-userpool-emailverificationsubject"></a>
A string representing the email verification subject\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LambdaConfig`  <a name="cfn-cognito-userpool-lambdaconfig"></a>
The AWS Lambda trigger configuration information for the Amazon Cognito user pool\.  
*Required*: No  
*Type*: [Amazon Cognito UserPool LambdaConfig](aws-properties-cognito-userpool-lambdaconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MfaConfiguration`  <a name="cfn-cognito-userpool-mfaconfiguration"></a>
Specifies multi\-factor authentication \(MFA\) configuration details\. Can be one of the following values:  
`OFF` \- MFA tokens are not required and cannot be specified during user registration\.  
`ON` \- MFA tokens are required for all user registrations\. You can only specify required when you are initially creating a user pool\.  
`OPTIONAL` \- Users have the option when registering to create an MFA token\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Policies`  <a name="cfn-cognito-userpool-policies"></a>
The policies associated with the Amazon Cognito user pool\.  
*Required*: No  
*Type*: [Amazon Cognito UserPool Policies](aws-properties-cognito-userpool-policies.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UserPoolName`  <a name="cfn-cognito-userpool-poolname"></a>
A string used to name the user pool\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Schema`  <a name="cfn-cognito-userpool-schema"></a>
A list of schema attributes for the new user pool\. These attributes can be standard or custom attributes\.  
*Required*: No  
*Type*: List of [SchemaAttribute](aws-properties-cognito-userpool-schemaattribute.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SmsAuthenticationMessage`  <a name="cfn-cognito-userpool-smsauthenticationmessage"></a>
A string representing the SMS authentication message\. Must contain `{####}` in the message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SmsConfiguration`  <a name="cfn-cognito-userpool-smsconfiguration"></a>
The Short Message Service \(SMS\) configuration\.  
*Required*: No  
*Type*: [Amazon Cognito UserPool SmsConfiguration](aws-properties-cognito-userpool-smsconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SmsVerificationMessage`  <a name="cfn-cognito-userpool-smsverificationmessage"></a>
A string representing the SMS verification message\. Must contain `{####}` in the message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UserPoolTags`  <a name="cfn-cognito-userpool-userpooltags"></a>
The cost allocation tags for the user pool\. For more information, see [Adding Cost Allocation Tags to Your User Pool](http://docs.aws.amazon.com//cognito/latest/developerguide/cognito-user-pools-cost-allocation-tagging.html) in the *Amazon Cognito Developer Guide*\.  
*Required*: No  
*Type*: String to String map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d279c11"></a>

### Ref<a name="w3ab2c21c10d279c11b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns a generated ID, such as `us-east-2_zgaEXAMPLE`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d279c11b5"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`ProviderName`  
The provider name of the Amazon Cognito user pool, specified as a `String`\.

`ProviderURL`  
The URL of the provider of the Amazon Cognito user pool, specified as a `String`\.

`Arn`  
The Amazon Resource Name \(ARN\) of the user pool, such as `arn:aws:cognito-idp:``us-east-2``:123412341234:userpool/us-east-1 _123412341`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.