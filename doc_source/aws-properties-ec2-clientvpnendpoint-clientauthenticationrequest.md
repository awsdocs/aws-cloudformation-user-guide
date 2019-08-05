# AWS::EC2::ClientVpnEndpoint ClientAuthenticationRequest<a name="aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest"></a>

Describes the authentication method to be used by a Client VPN endpoint\. Client VPN supports Active Directory and mutual authentication\. For more information, see [Authentication](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/authentication-authrization.html#client-authentication) in the *AWS Client VPN Administrator Guide*\.

## Syntax<a name="aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest-syntax.json"></a>

```
{
  "[ActiveDirectory](#cfn-ec2-clientvpnendpoint-clientauthenticationrequest-activedirectory)" : [DirectoryServiceAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest.md),
  "[MutualAuthentication](#cfn-ec2-clientvpnendpoint-clientauthenticationrequest-mutualauthentication)" : [CertificateAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest.md),
  "[Type](#cfn-ec2-clientvpnendpoint-clientauthenticationrequest-type)" : String
}
```

### YAML<a name="aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest-syntax.yaml"></a>

```
  [ActiveDirectory](#cfn-ec2-clientvpnendpoint-clientauthenticationrequest-activedirectory):
    [DirectoryServiceAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest.md)
  [MutualAuthentication](#cfn-ec2-clientvpnendpoint-clientauthenticationrequest-mutualauthentication):
    [CertificateAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest.md)
  [Type](#cfn-ec2-clientvpnendpoint-clientauthenticationrequest-type): String
```

## Properties<a name="aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest-properties"></a>

`ActiveDirectory`  <a name="cfn-ec2-clientvpnendpoint-clientauthenticationrequest-activedirectory"></a>
Information about the Active Directory to be used, if applicable\. You must provide this information if **Type** is `directory-service-authentication`\.
*Required*: No
*Type*: [DirectoryServiceAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MutualAuthentication`  <a name="cfn-ec2-clientvpnendpoint-clientauthenticationrequest-mutualauthentication"></a>
Information about the authentication certificates to be used, if applicable\. You must provide this information if **Type** is `certificate-authentication`\.
*Required*: No
*Type*: [CertificateAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ec2-clientvpnendpoint-clientauthenticationrequest-type"></a>
The type of client authentication to be used\. Specify `certificate-authentication` to use certificate\-based authentication, or `directory-service-authentication` to use Active Directory authentication\.
*Required*: Yes
*Type*: String
*Allowed Values*: `certificate-authentication | directory-service-authentication`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
