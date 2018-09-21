# Amazon Cognito UserPool AdminCreateUserConfig<a name="aws-properties-cognito-userpool-admincreateuserconfig"></a>

`AdminCreateUserConfig` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource\. The `AdminCreateUserConfig` property configures the `AdminCreateUser` requests for an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-admincreateuserconfig-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-admincreateuserconfig-syntax.json"></a>

```
{
  "[AllowAdminCreateUserOnly](#cfn-cognito-userpool-admincreateuserconfig-allowadmincreateuseronly)" : Boolean,
  "[InviteMessageTemplate](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate)" : MessageTemplateType,
  "[UnusedAccountValidityDays](#cfn-cognito-userpool-admincreateuserconfig-unusedaccountvaliditydays)" : Number
}
```

### YAML<a name="aws-properties-cognito-userpool-admincreateuserconfig-syntax.yaml"></a>

```
[AllowAdminCreateUserOnly](#cfn-cognito-userpool-admincreateuserconfig-allowadmincreateuseronly): Boolean
[InviteMessageTemplate](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate): MessageTemplateType
[UnusedAccountValidityDays](#cfn-cognito-userpool-admincreateuserconfig-unusedaccountvaliditydays): Number
```

## Properties<a name="aws-properties-cognito-userpool-admincreateuserconfig-properties"></a>

`AllowAdminCreateUserOnly`  <a name="cfn-cognito-userpool-admincreateuserconfig-allowadmincreateuseronly"></a>
Set to True if only the administrator is allowed to create user profiles\. Set to False if users can sign themselves up via an app\.  
*Type*: Boolean  
*Required*: No

`InviteMessageTemplate`  <a name="cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate"></a>
The message template to be used for the welcome message to new users\.  
*Type*: [Amazon Cognito UserPool InviteMessageTemplate](aws-properties-cognito-userpool-admincreateuserconfig-invitemessagetemplate.md)  
*Required*: No

`UnusedAccountValidityDays`  <a name="cfn-cognito-userpool-admincreateuserconfig-unusedaccountvaliditydays"></a>
The user account expiration limit, in days, after which the account is no longer usable\. To reset the account after that time limit, you must call AdminCreateUser again, specifying `RESEND` for the `MessageAction` parameter\. The default value for this parameter is 7\.  
*Type*: Number  
*Required*: No