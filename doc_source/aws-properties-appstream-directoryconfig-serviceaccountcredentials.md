# AWS::AppStream::DirectoryConfig ServiceAccountCredentials<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials"></a>

The credentials for the service account used by the streaming instance to connect to the directory\.

## Syntax<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials-syntax.json"></a>

```
{
  "[AccountName](#cfn-appstream-directoryconfig-serviceaccountcredentials-accountname)" : String,
  "[AccountPassword](#cfn-appstream-directoryconfig-serviceaccountcredentials-accountpassword)" : String
}
```

### YAML<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials-syntax.yaml"></a>

```
  [AccountName](#cfn-appstream-directoryconfig-serviceaccountcredentials-accountname): String
  [AccountPassword](#cfn-appstream-directoryconfig-serviceaccountcredentials-accountpassword): String
```

## Properties<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials-properties"></a>

`AccountName`  <a name="cfn-appstream-directoryconfig-serviceaccountcredentials-accountname"></a>
The user name of the account\. This account must have the following privileges: create computer objects, join computers to the domain, and change/reset the password on descendant computer objects for the organizational units specified\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccountPassword`  <a name="cfn-appstream-directoryconfig-serviceaccountcredentials-accountpassword"></a>
The password for the account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `127`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)