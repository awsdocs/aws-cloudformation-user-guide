# AWS::Cognito::UserPool AdminCreateUserConfig<a name="aws-properties-cognito-userpool-admincreateuserconfig"></a>

The configuration for `AdminCreateUser` requests\.

## Syntax<a name="aws-properties-cognito-userpool-admincreateuserconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-admincreateuserconfig-syntax.json"></a>

```
{
  "[AllowAdminCreateUserOnly](#cfn-cognito-userpool-admincreateuserconfig-allowadmincreateuseronly)" : Boolean,
  "[InviteMessageTemplate](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate)" : InviteMessageTemplate,
  "[UnusedAccountValidityDays](#cfn-cognito-userpool-admincreateuserconfig-unusedaccountvaliditydays)" : Integer
}
```

### YAML<a name="aws-properties-cognito-userpool-admincreateuserconfig-syntax.yaml"></a>

```
  [AllowAdminCreateUserOnly](#cfn-cognito-userpool-admincreateuserconfig-allowadmincreateuseronly): Boolean
  [InviteMessageTemplate](#cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate): 
    InviteMessageTemplate
  [UnusedAccountValidityDays](#cfn-cognito-userpool-admincreateuserconfig-unusedaccountvaliditydays): Integer
```

## Properties<a name="aws-properties-cognito-userpool-admincreateuserconfig-properties"></a>

`AllowAdminCreateUserOnly`  <a name="cfn-cognito-userpool-admincreateuserconfig-allowadmincreateuseronly"></a>
Set to `True` if only the administrator is allowed to create user profiles\. Set to `False` if users can sign themselves up via an app\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InviteMessageTemplate`  <a name="cfn-cognito-userpool-admincreateuserconfig-invitemessagetemplate"></a>
The message template to be used for the welcome message to new users\.  
See also [Customizing User Invitation Messages](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pool-settings-message-customizations.html#cognito-user-pool-settings-user-invitation-message-customization)\.  
*Required*: No  
*Type*: [InviteMessageTemplate](aws-properties-cognito-userpool-invitemessagetemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnusedAccountValidityDays`  <a name="cfn-cognito-userpool-admincreateuserconfig-unusedaccountvaliditydays"></a>
The user account expiration limit, in days, after which the account is no longer usable\. To reset the account after that time limit, you must call `AdminCreateUser` again, specifying `"RESEND"` for the `MessageAction` parameter\. The default value for this parameter is 7\.   
If you set a value for `TemporaryPasswordValidityDays` in `PasswordPolicy`, that value will be used and `UnusedAccountValidityDays` will be deprecated for that user pool\. 
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `365`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)