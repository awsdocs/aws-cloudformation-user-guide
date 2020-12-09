# AWS::Cognito::UserPoolRiskConfigurationAttachment NotifyConfigurationType<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype"></a>

The notify configuration type\.

## Syntax<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-syntax.json"></a>

```
{
  "[BlockEmail](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-blockemail)" : NotifyEmailType,
  "[From](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-from)" : String,
  "[MfaEmail](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-mfaemail)" : NotifyEmailType,
  "[NoActionEmail](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-noactionemail)" : NotifyEmailType,
  "[ReplyTo](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-replyto)" : String,
  "[SourceArn](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-sourcearn)" : String
}
```

### YAML<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-syntax.yaml"></a>

```
  [BlockEmail](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-blockemail): 
    NotifyEmailType
  [From](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-from): String
  [MfaEmail](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-mfaemail): 
    NotifyEmailType
  [NoActionEmail](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-noactionemail): 
    NotifyEmailType
  [ReplyTo](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-replyto): String
  [SourceArn](#cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-sourcearn): String
```

## Properties<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-properties"></a>

`BlockEmail`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-blockemail"></a>
Email template used when a detected risk event is blocked\.  
*Required*: No  
*Type*: [NotifyEmailType](aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`From`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-from"></a>
The email address that is sending the email\. It must be either individually verified with Amazon SES, or from a domain that has been verified with Amazon SES\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MfaEmail`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-mfaemail"></a>
The MFA email template used when MFA is challenged as part of a detected risk\.  
*Required*: No  
*Type*: [NotifyEmailType](aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoActionEmail`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-noactionemail"></a>
The email template used when a detected risk event is allowed\.  
*Required*: No  
*Type*: [NotifyEmailType](aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplyTo`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-replyto"></a>
The destination to which the receiver of an email should reply to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceArn`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyconfigurationtype-sourcearn"></a>
The Amazon Resource Name \(ARN\) of the identity that is associated with the sending authorization policy\. It permits Amazon Cognito to send for the email address specified in the `From` parameter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)