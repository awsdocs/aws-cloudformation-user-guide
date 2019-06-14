# AWS::EC2::ClientVpnEndpoint CertificateAuthenticationRequest<a name="aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest"></a>

Information about the client certificate to be used for authentication\.

## Syntax<a name="aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest-syntax.json"></a>

```
{
  "[ClientRootCertificateChainArn](#cfn-ec2-clientvpnendpoint-certificateauthenticationrequest-clientrootcertificatechainarn)" : String
}
```

### YAML<a name="aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest-syntax.yaml"></a>

```
  [ClientRootCertificateChainArn](#cfn-ec2-clientvpnendpoint-certificateauthenticationrequest-clientrootcertificatechainarn): String
```

## Properties<a name="aws-properties-ec2-clientvpnendpoint-certificateauthenticationrequest-properties"></a>

`ClientRootCertificateChainArn`  <a name="cfn-ec2-clientvpnendpoint-certificateauthenticationrequest-clientrootcertificatechainarn"></a>
The ARN of the client certificate\. The certificate must be signed by a certificate authority \(CA\) and it must be provisioned in AWS Certificate Manager \(ACM\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)