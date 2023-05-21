# AWS::Transfer::Server IdentityProviderDetails<a name="aws-properties-transfer-server-identityproviderdetails"></a>

Required when `IdentityProviderType` is set to `AWS_DIRECTORY_SERVICE`, ` AWS_LAMBDA` or `API_GATEWAY`\. Accepts an array containing all of the information required to use a directory in `AWS_DIRECTORY_SERVICE` or invoke a customer\-supplied authentication API, including the API Gateway URL\. Not required when `IdentityProviderType` is set to `SERVICE_MANAGED`\.

## Syntax<a name="aws-properties-transfer-server-identityproviderdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-identityproviderdetails-syntax.json"></a>

```
{
  "[DirectoryId](#cfn-transfer-server-identityproviderdetails-directoryid)" : String,
  "[Function](#cfn-transfer-server-identityproviderdetails-function)" : String,
  "[InvocationRole](#cfn-transfer-server-identityproviderdetails-invocationrole)" : String,
  "[SftpAuthenticationMethods](#cfn-transfer-server-identityproviderdetails-sftpauthenticationmethods)" : String,
  "[Url](#cfn-transfer-server-identityproviderdetails-url)" : String
}
```

### YAML<a name="aws-properties-transfer-server-identityproviderdetails-syntax.yaml"></a>

```
  [DirectoryId](#cfn-transfer-server-identityproviderdetails-directoryid): String
  [Function](#cfn-transfer-server-identityproviderdetails-function): String
  [InvocationRole](#cfn-transfer-server-identityproviderdetails-invocationrole): String
  [SftpAuthenticationMethods](#cfn-transfer-server-identityproviderdetails-sftpauthenticationmethods): String
  [Url](#cfn-transfer-server-identityproviderdetails-url): String
```

## Properties<a name="aws-properties-transfer-server-identityproviderdetails-properties"></a>

`DirectoryId`  <a name="cfn-transfer-server-identityproviderdetails-directoryid"></a>
The identifier of the AWS Directory Service directory that you want to stop sharing\.  
*Required*: No  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^d-[0-9a-f]{10}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Function`  <a name="cfn-transfer-server-identityproviderdetails-function"></a>
The ARN for a Lambda function to use for the Identity provider\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `170`  
*Pattern*: `^arn:[a-z-]+:lambda:.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationRole`  <a name="cfn-transfer-server-identityproviderdetails-invocationrole"></a>
This parameter is only applicable if your `IdentityProviderType` is `API_GATEWAY`\. Provides the type of `InvocationRole` used to authenticate the user account\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SftpAuthenticationMethods`  <a name="cfn-transfer-server-identityproviderdetails-sftpauthenticationmethods"></a>
For SFTP\-enabled servers, and for custom identity providers *only*, you can specify whether to authenticate using a password, SSH key pair, or both\.  
+  `PASSWORD` \- users must provide their password to connect\.
+  `PUBLIC_KEY` \- users must provide their private key to connect\.
+  `PUBLIC_KEY_OR_PASSWORD` \- users can authenticate with either their password or their key\. This is the default value\.
+  `PUBLIC_KEY_AND_PASSWORD` \- users must provide both their private key and their password to connect\. The server checks the key first, and then if the key is valid, the system prompts for a password\. If the private key provided does not match the public key that is stored, authentication fails\.
*Required*: No  
*Type*: String  
*Allowed values*: `PASSWORD | PUBLIC_KEY | PUBLIC_KEY_AND_PASSWORD | PUBLIC_KEY_OR_PASSWORD`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-transfer-server-identityproviderdetails-url"></a>
Provides the location of the service endpoint used to authenticate users\.  
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-transfer-server-identityproviderdetails--seealso"></a>

[IdentityProviderDetails](https://docs.aws.amazon.com/transfer/latest/userguide/API_IdentityProviderDetails.html) in the *AWS Transfer Family User Guide*\.