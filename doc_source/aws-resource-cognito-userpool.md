# AWS::Cognito::UserPool<a name="aws-resource-cognito-userpool"></a>

The `AWS::Cognito::UserPool` resource creates an Amazon Cognito user pool\. For more information on working with Amazon Cognito user pools, see [Amazon Cognito User Pools](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html) and [CreateUserPool](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_CreateUserPool.html)\.

## Syntax<a name="aws-resource-cognito-userpool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpool-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPool",
  "Properties" : {
      "[AccountRecoverySetting](#cfn-cognito-userpool-accountrecoverysetting)" : AccountRecoverySetting,
      "[AdminCreateUserConfig](#cfn-cognito-userpool-admincreateuserconfig)" : AdminCreateUserConfig,
      "[AliasAttributes](#cfn-cognito-userpool-aliasattributes)" : [ String, ... ],
      "[AutoVerifiedAttributes](#cfn-cognito-userpool-autoverifiedattributes)" : [ String, ... ],
      "[DeviceConfiguration](#cfn-cognito-userpool-deviceconfiguration)" : DeviceConfiguration,
      "[EmailConfiguration](#cfn-cognito-userpool-emailconfiguration)" : EmailConfiguration,
      "[EmailVerificationMessage](#cfn-cognito-userpool-emailverificationmessage)" : String,
      "[EmailVerificationSubject](#cfn-cognito-userpool-emailverificationsubject)" : String,
      "[EnabledMfas](#cfn-cognito-userpool-enabledmfas)" : [ String, ... ],
      "[LambdaConfig](#cfn-cognito-userpool-lambdaconfig)" : LambdaConfig,
      "[MfaConfiguration](#cfn-cognito-userpool-mfaconfiguration)" : String,
      "[Policies](#cfn-cognito-userpool-policies)" : Policies,
      "[Schema](#cfn-cognito-userpool-schema)" : [ SchemaAttribute, ... ],
      "[SmsAuthenticationMessage](#cfn-cognito-userpool-smsauthenticationmessage)" : String,
      "[SmsConfiguration](#cfn-cognito-userpool-smsconfiguration)" : SmsConfiguration,
      "[SmsVerificationMessage](#cfn-cognito-userpool-smsverificationmessage)" : String,
      "[UsernameAttributes](#cfn-cognito-userpool-usernameattributes)" : [ String, ... ],
      "[UsernameConfiguration](#cfn-cognito-userpool-usernameconfiguration)" : UsernameConfiguration,
      "[UserPoolAddOns](#cfn-cognito-userpool-userpooladdons)" : UserPoolAddOns,
      "[UserPoolName](#cfn-cognito-userpool-userpoolname)" : String,
      "[UserPoolTags](#cfn-cognito-userpool-userpooltags)" : Json,
      "[VerificationMessageTemplate](#cfn-cognito-userpool-verificationmessagetemplate)" : VerificationMessageTemplate
    }
}
```

### YAML<a name="aws-resource-cognito-userpool-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPool
Properties: 
  [AccountRecoverySetting](#cfn-cognito-userpool-accountrecoverysetting): 
    AccountRecoverySetting
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
  [EnabledMfas](#cfn-cognito-userpool-enabledmfas): 
    - String
  [LambdaConfig](#cfn-cognito-userpool-lambdaconfig): 
    LambdaConfig
  [MfaConfiguration](#cfn-cognito-userpool-mfaconfiguration): String
  [Policies](#cfn-cognito-userpool-policies): 
    Policies
  [Schema](#cfn-cognito-userpool-schema): 
    - SchemaAttribute
  [SmsAuthenticationMessage](#cfn-cognito-userpool-smsauthenticationmessage): String
  [SmsConfiguration](#cfn-cognito-userpool-smsconfiguration): 
    SmsConfiguration
  [SmsVerificationMessage](#cfn-cognito-userpool-smsverificationmessage): String
  [UsernameAttributes](#cfn-cognito-userpool-usernameattributes): 
    - String
  [UsernameConfiguration](#cfn-cognito-userpool-usernameconfiguration): 
    UsernameConfiguration
  [UserPoolAddOns](#cfn-cognito-userpool-userpooladdons): 
    UserPoolAddOns
  [UserPoolName](#cfn-cognito-userpool-userpoolname): String
  [UserPoolTags](#cfn-cognito-userpool-userpooltags): Json
  [VerificationMessageTemplate](#cfn-cognito-userpool-verificationmessagetemplate): 
    VerificationMessageTemplate
```

## Properties<a name="aws-resource-cognito-userpool-properties"></a>

`AccountRecoverySetting`  <a name="cfn-cognito-userpool-accountrecoverysetting"></a>
Use this setting to define which verified available method a user can use to recover their password when they call `ForgotPassword`\. It allows you to define a preferred method when a user has more than one method available\. With this setting, SMS does not qualify for a valid password recovery mechanism if the user also has SMS MFA enabled\. In the absence of this setting, Cognito uses the legacy behavior to determine the recovery method where SMS is preferred over email\.  
*Required*: No  
*Type*: [AccountRecoverySetting](aws-properties-cognito-userpool-accountrecoverysetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdminCreateUserConfig`  <a name="cfn-cognito-userpool-admincreateuserconfig"></a>
The configuration for creating a new user profile\.  
*Required*: No  
*Type*: [AdminCreateUserConfig](aws-properties-cognito-userpool-admincreateuserconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AliasAttributes`  <a name="cfn-cognito-userpool-aliasattributes"></a>
Attributes supported as an alias for this user pool\. Possible values: **phone\_number**, **email**, or **preferred\_username**\.  
This user pool property cannot be updated\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoVerifiedAttributes`  <a name="cfn-cognito-userpool-autoverifiedattributes"></a>
The attributes to be auto\-verified\. Possible values: **email**, **phone\_number**\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceConfiguration`  <a name="cfn-cognito-userpool-deviceconfiguration"></a>
The device configuration\.  
*Required*: No  
*Type*: [DeviceConfiguration](aws-properties-cognito-userpool-deviceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailConfiguration`  <a name="cfn-cognito-userpool-emailconfiguration"></a>
The email configuration\.  
*Required*: No  
*Type*: [EmailConfiguration](aws-properties-cognito-userpool-emailconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailVerificationMessage`  <a name="cfn-cognito-userpool-emailverificationmessage"></a>
A string representing the email verification message\. EmailVerificationMessage is allowed only if [EmailSendingAccount](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_EmailConfigurationType.html#CognitoUserPools-Type-EmailConfigurationType-EmailSendingAccount) is DEVELOPER\.   
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `20000`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]*\{####\}[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailVerificationSubject`  <a name="cfn-cognito-userpool-emailverificationsubject"></a>
A string representing the email verification subject\. EmailVerificationSubject is allowed only if [EmailSendingAccount](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_EmailConfigurationType.html#CognitoUserPools-Type-EmailConfigurationType-EmailSendingAccount) is DEVELOPER\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnabledMfas`  <a name="cfn-cognito-userpool-enabledmfas"></a>
Enables MFA on a specified user pool\. To disable all MFAs after it has been enabled, set MfaConfiguration to “OFF” and remove EnabledMfas\. MFAs can only be all disabled if MfaConfiguration is OFF\. Once SMS\_MFA is enabled, SMS\_MFA can only be disabled by setting MfaConfiguration to “OFF”\. Can be one of the following values:  
+ `SMS_MFA` \- Enables SMS MFA for the user pool\. SMS\_MFA can only be enabled if SMS configuration is provided\.
+ `SOFTWARE_TOKEN_MFA` \- Enables software token MFA for the user pool\.
Allowed values: `SMS_MFA` \| `SOFTWARE_TOKEN_MFA`  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaConfig`  <a name="cfn-cognito-userpool-lambdaconfig"></a>
The Lambda trigger configuration information for the new user pool\.  
In a push model, event sources \(such as Amazon S3 and custom applications\) need permission to invoke a function\. So you will need to make an extra call to add permission for these event sources to invoke your Lambda function\.  
  
For more information on using the Lambda API to add permission, see [ AddPermission ](https://docs.aws.amazon.com/lambda/latest/dg/API_AddPermission.html)\.   
For adding permission using the AWS CLI, see [ add\-permission ](https://docs.aws.amazon.com/cli/latest/reference/lambda/add-permission.html)\.
*Required*: No  
*Type*: [LambdaConfig](aws-properties-cognito-userpool-lambdaconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MfaConfiguration`  <a name="cfn-cognito-userpool-mfaconfiguration"></a>
The multi\-factor \(MFA\) configuration\. Valid values include:  
+  `OFF` MFA will not be used for any users\.
+  `ON` MFA is required for all users to sign in\.
+  `OPTIONAL` MFA will be required only for individual users who have an MFA factor enabled\.
*Required*: No  
*Type*: String  
*Allowed values*: `OFF | ON | OPTIONAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policies`  <a name="cfn-cognito-userpool-policies"></a>
The policy associated with a user pool\.  
*Required*: No  
*Type*: [Policies](aws-properties-cognito-userpool-policies.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schema`  <a name="cfn-cognito-userpool-schema"></a>
The schema attributes for the new user pool\. These attributes can be standard or custom attributes\.  
 During a user pool update, you can add new schema attributes but you cannot modify or delete an existing schema attribute\.
*Required*: No  
*Type*: List of [SchemaAttribute](aws-properties-cognito-userpool-schemaattribute.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmsAuthenticationMessage`  <a name="cfn-cognito-userpool-smsauthenticationmessage"></a>
A string representing the SMS authentication message\.  
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `140`  
*Pattern*: `.*\{####\}.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmsConfiguration`  <a name="cfn-cognito-userpool-smsconfiguration"></a>
The SMS configuration\.  
*Required*: No  
*Type*: [SmsConfiguration](aws-properties-cognito-userpool-smsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmsVerificationMessage`  <a name="cfn-cognito-userpool-smsverificationmessage"></a>
A string representing the SMS verification message\.  
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `140`  
*Pattern*: `.*\{####\}.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsernameAttributes`  <a name="cfn-cognito-userpool-usernameattributes"></a>
Determines whether email addresses or phone numbers can be specified as user names when a user signs up\. Possible values: `phone_number` or `email`\.  
This user pool property cannot be updated\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsernameConfiguration`  <a name="cfn-cognito-userpool-usernameconfiguration"></a>
You can choose to set case sensitivity on the username input for the selected sign\-in option\. For example, when this is set to `False`, users will be able to sign in using either "username" or "Username"\. This configuration is immutable once it has been set\.  
*Required*: No  
*Type*: [UsernameConfiguration](aws-properties-cognito-userpool-usernameconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolAddOns`  <a name="cfn-cognito-userpool-userpooladdons"></a>
Used to enable advanced security risk detection\. Set the key `AdvancedSecurityMode` to the value "AUDIT"\.  
*Required*: No  
*Type*: [UserPoolAddOns](aws-properties-cognito-userpool-userpooladdons.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolName`  <a name="cfn-cognito-userpool-userpoolname"></a>
A string used to name the user pool\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w\s+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolTags`  <a name="cfn-cognito-userpool-userpooltags"></a>
The tag keys and values to assign to the user pool\. A tag is a label that you can use to categorize and manage user pools in different ways, such as by purpose, owner, environment, or other criteria\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerificationMessageTemplate`  <a name="cfn-cognito-userpool-verificationmessagetemplate"></a>
The template for the verification message that the user sees when the app requests permission to access the user's information\.  
*Required*: No  
*Type*: [VerificationMessageTemplate](aws-properties-cognito-userpool-verificationmessagetemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cognito-userpool-return-values"></a>

### Ref<a name="aws-resource-cognito-userpool-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a generated ID, such as `us-east-2_zgaEXAMPLE`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cognito-userpool-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cognito-userpool-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the user pool, such as `arn:aws:cognito-idp:us-east-1:123412341234:userpool/us-east-1_123412341`\.

`ProviderName`  <a name="ProviderName-fn::getatt"></a>
The provider name of the Amazon Cognito user pool, specified as a `String`\.

`ProviderURL`  <a name="ProviderURL-fn::getatt"></a>
The URL of the provider of the Amazon Cognito user pool, specified as a `String`\.