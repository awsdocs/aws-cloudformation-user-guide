# Amazon AppStream 2\.0 DirectoryConfig ServiceAccountCredentials<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials"></a>

<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials-description"></a>The `ServiceAccountCredentials` property type specifies the credentials for the service account used by the streaming instance to connect to the directory\. 

<a name="aws-properties-appstream-directoryconfig-serviceaccountcredentials-inheritance"></a> `ServiceAccountCredentials` is a property of the [AWS::AppStream::DirectoryConfig](aws-resource-appstream-directoryconfig.md) resource\.

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
The user name of the account\. This account must have the following permissions: create computer objects, join computers to the domain, and change/reset the password on descendant computer objects for the organizational units specified\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AccountPassword`  <a name="cfn-appstream-directoryconfig-serviceaccountcredentials-accountpassword"></a>
The password for the account\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 