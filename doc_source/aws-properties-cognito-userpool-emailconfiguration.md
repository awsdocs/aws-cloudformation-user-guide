# AWS::Cognito::UserPool EmailConfiguration<a name="aws-properties-cognito-userpool-emailconfiguration"></a>

`EmailConfiguration` is a property of the [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html) resource that defines the email configuration of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-emailconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-emailconfiguration-syntax.json"></a>

```
{
  "[EmailSendingAccount](#cfn-cognito-userpool-emailconfiguration-emailsendingaccount)" : String,
  "[ReplyToEmailAddress](#cfn-cognito-userpool-emailconfiguration-replytoemailaddress)" : String,
  "[SourceArn](#cfn-cognito-userpool-emailconfiguration-sourcearn)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-emailconfiguration-syntax.yaml"></a>

```
﻿  [EmailSendingAccount](#cfn-cognito-userpool-emailconfiguration-emailsendingaccount) : String
﻿  [ReplyToEmailAddress](#cfn-cognito-userpool-emailconfiguration-replytoemailaddress) : String
﻿  [SourceArn](#cfn-cognito-userpool-emailconfiguration-sourcearn) : String
```

## Properties<a name="aws-properties-cognito-userpool-emailconfiguration-properties"></a>

`EmailSendingAccount`  <a name="cfn-cognito-userpool-emailconfiguration-emailsendingaccount"></a>
Specifies whether Amazon Cognito emails your users by using its built\-in email functionality or your Amazon SES email configuration\. Specify one of the following values:    
COGNITO\_DEFAULT  
When Amazon Cognito emails your users, it uses its built\-in email functionality\. When you use the default option, Amazon Cognito allows only a limited number of emails each day for your user pool\. For typical production environments, the default email limit is below the required delivery volume\. To achieve a higher delivery volume, specify DEVELOPER to use your Amazon SES email configuration\.  
To look up the email delivery limit for the default option, see [Limits in Amazon Cognito](https://docs.aws.amazon.com/cognito/latest/developerguide/limits.html) in the *Amazon Cognito Developer Guide*\.  
The default FROM address is no\-reply@verificationemail\.com\. To customize the FROM address, provide the ARN of an Amazon SES verified email address for the `SourceArn` parameter\.  
DEVELOPER  
When Amazon Cognito emails your users, it uses your Amazon SES configuration\. Amazon Cognito calls Amazon SES on your behalf to send email from your verified email address\. When you use this option, the email delivery limits are the same limits that apply to your Amazon SES verified email address in your AWS account\.  
If you use this option, you must provide the ARN of an Amazon SES verified email address for the `SourceArn` parameter\.  
Before Amazon Cognito can email your users, it requires additional permissions to call Amazon SES on your behalf\. When you update your user pool with this option, Amazon Cognito creates a *service\-linked role*, which is a type of IAM role, in your AWS account\. This role contains the permissions that allow Amazon Cognito to access Amazon SES and send email messages with your address\. For more information about the service\-linked role that Amazon Cognito creates, see [Using Service\-Linked Roles for Amazon Cognito](https://docs.aws.amazon.com/cognito/latest/developerguide/using-service-linked-roles.html) in the *Amazon Cognito Developer Guide*\.
*Required*: No  
*Type*: String  
*Allowed Values*: `COGNITO_DEFAULT | DEVELOPER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplyToEmailAddress`  <a name="cfn-cognito-userpool-emailconfiguration-replytoemailaddress"></a>
The destination to which the receiver of the email should reply to\.  
*Required*: No  
*Type*: String  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}]+@[\p{L}\p{M}\p{S}\p{N}\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceArn`  <a name="cfn-cognito-userpool-emailconfiguration-sourcearn"></a>
The Amazon Resource Name \(ARN\) of a verified email address in Amazon SES\. This email address is used in one of the following ways, depending on the value that you specify for the `EmailSendingAccount` parameter:  
+ If you specify `COGNITO_DEFAULT`, Amazon Cognito uses this address as the custom FROM address when it emails your users by using its built\-in email account\.
+ If you specify `DEVELOPER`, Amazon Cognito emails your users with this address by calling Amazon SES on your behalf\.
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)