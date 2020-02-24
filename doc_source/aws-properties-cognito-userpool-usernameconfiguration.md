# AWS::Cognito::UserPool UsernameConfiguration<a name="aws-properties-cognito-userpool-usernameconfiguration"></a>

Used to configure username case insensitivity\.

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
Set to `False` if you want `username`, `email` alias and `preferred_username` alias to be case insensitive\. For example, when set to `False`, users will be able to sign in using either "username" or "Username"\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)