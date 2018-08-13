# IAM User LoginProfile<a name="aws-properties-iam-user-loginprofile"></a>

`LoginProfile` is a property of the [AWS::IAM::User](aws-properties-iam-user.md) resource that creates a login profile for users so that they can access the AWS Management Console\.

## Syntax<a name="w3ab2c21c14e1312b5"></a>

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

## Properties<a name="w3ab2c21c14e1312b7"></a>

`Password`  <a name="cfn-iam-user-loginprofile-password"></a>
The password for the user\.  
*Required*: Yes  
*Type*: String

`PasswordResetRequired`  <a name="cfn-iam-user-loginprofile-passwordresetrequired"></a>
Specifies whether the user is required to set a new password the next time the user logs in to the AWS Management Console\.  
*Required*: No  
*Type*: Boolean