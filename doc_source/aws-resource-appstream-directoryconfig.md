# AWS::AppStream::DirectoryConfig<a name="aws-resource-appstream-directoryconfig"></a>

The `AWS::AppStream::DirectoryConfig` resource specifies the configuration information required to join Amazon AppStream 2\.0 fleets and image builders to Microsoft Active Directory domains\. 

## Syntax<a name="aws-resource-appstream-directoryconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-directoryconfig-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::DirectoryConfig",
  "Properties" : {
      "[DirectoryName](#cfn-appstream-directoryconfig-directoryname)" : String,
      "[OrganizationalUnitDistinguishedNames](#cfn-appstream-directoryconfig-organizationalunitdistinguishednames)" : [ String, ... ],
      "[ServiceAccountCredentials](#cfn-appstream-directoryconfig-serviceaccountcredentials)" : ServiceAccountCredentials
    }
}
```

### YAML<a name="aws-resource-appstream-directoryconfig-syntax.yaml"></a>

```
Type: AWS::AppStream::DirectoryConfig
Properties: 
  [DirectoryName](#cfn-appstream-directoryconfig-directoryname): String
  [OrganizationalUnitDistinguishedNames](#cfn-appstream-directoryconfig-organizationalunitdistinguishednames): 
    - String
  [ServiceAccountCredentials](#cfn-appstream-directoryconfig-serviceaccountcredentials): 
    ServiceAccountCredentials
```

## Properties<a name="aws-resource-appstream-directoryconfig-properties"></a>

`DirectoryName`  <a name="cfn-appstream-directoryconfig-directoryname"></a>
The fully qualified name of the directory \(for example, corp\.example\.com\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrganizationalUnitDistinguishedNames`  <a name="cfn-appstream-directoryconfig-organizationalunitdistinguishednames"></a>
The distinguished names of the organizational units for computer accounts\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccountCredentials`  <a name="cfn-appstream-directoryconfig-serviceaccountcredentials"></a>
The credentials for the service account used by the streaming instance to connect to the directory\. Do not use this parameter directly\. Use `ServiceAccountCredentials` as an input parameter with `noEcho` as shown in the [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\. For best practices information, see [Do Not Embed Credentials in Your Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds)\.   
*Required*: Yes  
*Type*: [ServiceAccountCredentials](aws-properties-appstream-directoryconfig-serviceaccountcredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-resource-appstream-directoryconfig--seealso"></a>
+  [CreateDirectoryConfig](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateDirectoryConfig.html) in the *Amazon AppStream 2\.0 API Reference* 

