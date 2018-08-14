# Amazon Cognito UserPool InviteMessageTemplate<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate"></a>

`InviteMessageTemplate` is a subproperty of the [Amazon Cognito UserPool AdminCreateUserConfig](aws-properties-cognito-userpool-admincreateuserconfig.md) property that defines the email and SMS invitation message structure of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-syntax.json"></a>

```
{
  "[EmailMessage](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailmessage)" : String,
  "[EmailSubject](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailsubject)" : String,
  "[SMSMessage](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-smsmessage)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-syntax.yaml"></a>

```
[EmailMessage](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailmessage): String
[EmailSubject](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailsubject): String
[SMSMessage](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-smsmessage): String
```

## Properties<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-properties"></a>

`EmailMessage`  <a name="cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailmessage"></a>
The message template for email messages\.  
*Type*: String  
*Required*: No

`EmailSubject`  <a name="cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailsubject"></a>
The subject line for email messages\.  
*Type*: String  
*Required*: No

`SMSMessage`  <a name="cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-smsmessage"></a>
The message template for SMS messages\.  
*Type*: String  
*Required*: No