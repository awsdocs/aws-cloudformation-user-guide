# AWS::Cognito::UserPool UsernameConfiguration<a name="aws-properties-cognito-userpool-usernameconfiguration"></a>

The `UsernameConfiguration` property type specifies case sensitivity on the username input for the selected sign\-in option\.

## Syntax<a name="aws-properties-cognito-userpool-usernameconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-usernameconfiguration-syntax.json"></a>

```
{
  "[CaseSensitive](#cfn-cognito-userpool-usernameconfiguration-casesensitive)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpool-usernameconfiguration-syntax.yaml"></a>

```
  [CaseSensitive](#cfn-cognito-userpool-usernameconfiguration-casesensitive): Boolean
```

## Properties<a name="aws-properties-cognito-userpool-usernameconfiguration-properties"></a>

`CaseSensitive`  <a name="cfn-cognito-userpool-usernameconfiguration-casesensitive"></a>
Specifies whether user name case sensitivity will be applied for all users in the user pool through Amazon Cognito APIs\. For most use cases, set case sensitivity to `False` \(case insensitive\) as a best practice\. When usernames and email addresses are case insensitive, users can sign in as the same user when they enter a different capitalization of their user name\.  
Valid values include:    
True  
Enables case sensitivity for all username input\. When this option is set to `True`, users must sign in using the exact capitalization of their given username, such as “UserName”\. This is the default value\.  
False  
Enables case insensitivity for all username input\. For example, when this option is set to `False`, users can sign in using `username`, `USERNAME`, or `UserName`\. This option also enables both `preferred_username` and `email` alias to be case insensitive, in addition to the `username` attribute\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)