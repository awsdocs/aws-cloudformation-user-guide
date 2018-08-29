# Amazon Cognito UserPool InviteMessageTemplate<a name="aws-properties-cognito-userpool-invitemessagetemplate"></a>

`InviteMessageTemplate` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the email invitation message template of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-invitemessagetemplate-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-invitemessagetemplate-syntax.json"></a>

```
{
  "[EmailMessage](#cfn-cognito-userpool-invitemessagetemplate-emailmessage)" : String,
  "[EmailSubject](#cfn-cognito-userpool-invitemessagetemplate-emailsubject)" : String,
  "[SMSMessage](#cfn-cognito-userpool-invitemessagetemplate-smsmessage)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-invitemessagetemplate-syntax.yaml"></a>

```
[EmailMessage](#cfn-cognito-userpool-invitemessagetemplate-emailmessage): String
[EmailSubject](#cfn-cognito-userpool-invitemessagetemplate-emailsubject): String
[SMSMessage](#cfn-cognito-userpool-invitemessagetemplate-smsmessage): String
```

## Properties<a name="aws-properties-cognito-userpool-invitemessagetemplate-properties"></a>

`EmailMessage`  <a name="cfn-cognito-userpool-invitemessagetemplate-emailmessage"></a>
The message template for email messages\.  
*Type*: String  
*Required*: No

`EmailSubject`  <a name="cfn-cognito-userpool-invitemessagetemplate-emailsubject"></a>
The subject line for email messages\.  
*Type*: String  
*Required*: No

`SMSMessage`  <a name="cfn-cognito-userpool-invitemessagetemplate-smsmessage"></a>
The message template for SMS messages\.  
*Type*: String  
*Required*: No