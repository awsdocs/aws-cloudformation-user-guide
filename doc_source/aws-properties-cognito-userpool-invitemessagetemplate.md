# Amazon Cognito UserPool InviteMessageTemplate<a name="aws-properties-cognito-userpool-invitemessagetemplate"></a>

`InviteMessageTemplate` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the email invitation message template of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-invitemessagetemplate-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-invitemessagetemplate-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-invitemessagetemplate-emailmessage)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-invitemessagetemplate-emailsubject)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-invitemessagetemplate-smsmessage)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-invitemessagetemplate-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-invitemessagetemplate-emailmessage): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-invitemessagetemplate-emailsubject): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-invitemessagetemplate-smsmessage): String
```

## Properties<a name="aws-properties-cognito-userpool-invitemessagetemplate-properties"></a>

`EmailMessage`  
The message template for email messages\.  
*Type*: String  
*Required: *No

`EmailSubject`  
The subject line for email messages\.  
*Type*: String  
*Required: *No

`SMSMessage`  
The message template for SMS messages\.  
*Type*: String  
*Required: *No