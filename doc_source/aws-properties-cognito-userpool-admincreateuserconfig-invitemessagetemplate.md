# Amazon Cognito UserPool InviteMessageTemplate<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate"></a>

`InviteMessageTemplate` is a subproperty of the [Amazon Cognito UserPool AdminCreateUserConfig](aws-properties-cognito-userpool-admincreateuserconfig.md) property that defines the email and SMS invitation message structure of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailmessage)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailsubject)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-smsmessage)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailmessage): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-emailsubject): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate-smsmessage): String
```

## Properties<a name="aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate-properties"></a>

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