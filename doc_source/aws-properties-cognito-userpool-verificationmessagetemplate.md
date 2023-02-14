# AWS::Cognito::UserPool VerificationMessageTemplate<a name="aws-properties-cognito-userpool-verificationmessagetemplate"></a>

The template for verification messages\.

## Syntax<a name="aws-properties-cognito-userpool-verificationmessagetemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-verificationmessagetemplate-syntax.json"></a>

```
{
  "[DefaultEmailOption](#cfn-cognito-userpool-verificationmessagetemplate-defaultemailoption)" : String,
  "[EmailMessage](#cfn-cognito-userpool-verificationmessagetemplate-emailmessage)" : String,
  "[EmailMessageByLink](#cfn-cognito-userpool-verificationmessagetemplate-emailmessagebylink)" : String,
  "[EmailSubject](#cfn-cognito-userpool-verificationmessagetemplate-emailsubject)" : String,
  "[EmailSubjectByLink](#cfn-cognito-userpool-verificationmessagetemplate-emailsubjectbylink)" : String,
  "[SmsMessage](#cfn-cognito-userpool-verificationmessagetemplate-smsmessage)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-verificationmessagetemplate-syntax.yaml"></a>

```
  [DefaultEmailOption](#cfn-cognito-userpool-verificationmessagetemplate-defaultemailoption): String
  [EmailMessage](#cfn-cognito-userpool-verificationmessagetemplate-emailmessage): String
  [EmailMessageByLink](#cfn-cognito-userpool-verificationmessagetemplate-emailmessagebylink): String
  [EmailSubject](#cfn-cognito-userpool-verificationmessagetemplate-emailsubject): String
  [EmailSubjectByLink](#cfn-cognito-userpool-verificationmessagetemplate-emailsubjectbylink): String
  [SmsMessage](#cfn-cognito-userpool-verificationmessagetemplate-smsmessage): String
```

## Properties<a name="aws-properties-cognito-userpool-verificationmessagetemplate-properties"></a>

`DefaultEmailOption`  <a name="cfn-cognito-userpool-verificationmessagetemplate-defaultemailoption"></a>
The default email option\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CONFIRM_WITH_CODE | CONFIRM_WITH_LINK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailMessage`  <a name="cfn-cognito-userpool-verificationmessagetemplate-emailmessage"></a>
The email message template\. EmailMessage is allowed only if [ EmailSendingAccount](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_EmailConfigurationType.html#CognitoUserPools-Type-EmailConfigurationType-EmailSendingAccount) is DEVELOPER\.   
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `20000`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]*\{####\}[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailMessageByLink`  <a name="cfn-cognito-userpool-verificationmessagetemplate-emailmessagebylink"></a>
The email message template for sending a confirmation link to the user\. EmailMessageByLink is allowed only if [ EmailSendingAccount](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_EmailConfigurationType.html#CognitoUserPools-Type-EmailConfigurationType-EmailSendingAccount) is DEVELOPER\.  
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `20000`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]*\{##[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]*##\}[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailSubject`  <a name="cfn-cognito-userpool-verificationmessagetemplate-emailsubject"></a>
The subject line for the email message template\. EmailSubject is allowed only if [EmailSendingAccount](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_EmailConfigurationType.html#CognitoUserPools-Type-EmailConfigurationType-EmailSendingAccount) is DEVELOPER\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailSubjectByLink`  <a name="cfn-cognito-userpool-verificationmessagetemplate-emailsubjectbylink"></a>
The subject line for the email message template for sending a confirmation link to the user\. EmailSubjectByLink is allowed only [ EmailSendingAccount](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_EmailConfigurationType.html#CognitoUserPools-Type-EmailConfigurationType-EmailSendingAccount) is DEVELOPER\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmsMessage`  <a name="cfn-cognito-userpool-verificationmessagetemplate-smsmessage"></a>
The SMS message template\.  
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `140`  
*Pattern*: `.*\{####\}.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)