# AWS::AppStream::DirectoryConfig CertificateBasedAuthProperties<a name="aws-properties-appstream-directoryconfig-certificatebasedauthproperties"></a>

The certificate\-based authentication properties used to authenticate SAML 2\.0 Identity Provider \(IdP\) user identities to Active Directory domain\-joined streaming instances\. 

## Syntax<a name="aws-properties-appstream-directoryconfig-certificatebasedauthproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-directoryconfig-certificatebasedauthproperties-syntax.json"></a>

```
{
  "[CertificateAuthorityArn](#cfn-appstream-directoryconfig-certificatebasedauthproperties-certificateauthorityarn)" : String,
  "[Status](#cfn-appstream-directoryconfig-certificatebasedauthproperties-status)" : String
}
```

### YAML<a name="aws-properties-appstream-directoryconfig-certificatebasedauthproperties-syntax.yaml"></a>

```
  [CertificateAuthorityArn](#cfn-appstream-directoryconfig-certificatebasedauthproperties-certificateauthorityarn): String
  [Status](#cfn-appstream-directoryconfig-certificatebasedauthproperties-status): String
```

## Properties<a name="aws-properties-appstream-directoryconfig-certificatebasedauthproperties-properties"></a>

`CertificateAuthorityArn`  <a name="cfn-appstream-directoryconfig-certificatebasedauthproperties-certificateauthorityarn"></a>
The ARN of the AWS Certificate Manager Private CA resource\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws(?:\-cn|\-iso\-b|\-iso|\-us\-gov)?:[A-Za-z0-9][A-Za-z0-9_/.-]{0,62}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9][A-Za-z0-9:_/+=,@.\\-]{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-appstream-directoryconfig-certificatebasedauthproperties-status"></a>
The status of the certificate\-based authentication properties\. Fallback is turned on by default when certificate\-based authentication is **Enabled**\. Fallback allows users to log in using their AD domain password if certificate\-based authentication is unsuccessful, or to unlock a desktop lock screen\. **Enabled\_no\_directory\_login\_fallback** enables certificate\-based authentication, but does not allow users to log in using their AD domain password\. Users will be disconnected to re\-authenticate using certificates\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED | ENABLED_NO_DIRECTORY_LOGIN_FALLBACK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)