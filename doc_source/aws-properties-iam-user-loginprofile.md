# AWS::IAM::User LoginProfile<a name="aws-properties-iam-user-loginprofile"></a>

Contains the user name and password create date for a user\.

## Syntax<a name="aws-properties-iam-user-loginprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iam-user-loginprofile-syntax.json"></a>

```
{
  "[Password](#cfn-iam-user-loginprofile-password)" : String,
  "[PasswordResetRequired](#cfn-iam-user-loginprofile-passwordresetrequired)" : Boolean
}
```

### YAML<a name="aws-properties-iam-user-loginprofile-syntax.yaml"></a>

```
  [Password](#cfn-iam-user-loginprofile-password): String
  [PasswordResetRequired](#cfn-iam-user-loginprofile-passwordresetrequired): Boolean
```

## Properties<a name="aws-properties-iam-user-loginprofile-properties"></a>

`Password`  <a name="cfn-iam-user-loginprofile-password"></a>
The user's password\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PasswordResetRequired`  <a name="cfn-iam-user-loginprofile-passwordresetrequired"></a>
Specifies whether the user is required to set a new password on next sign\-in\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-iam-user-loginprofile--seealso"></a>
+  [LoginProfile](https://docs.aws.amazon.com/IAM/latest/APIReference/API_LoginProfile.html) in the *AWS Identity and Access Management API Reference* 

