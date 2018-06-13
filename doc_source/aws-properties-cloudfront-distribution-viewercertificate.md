# CloudFront Distribution ViewerCertificate<a name="aws-properties-cloudfront-distribution-viewercertificate"></a>

`ViewerCertificate` is a property of the [CloudFront Distribution DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md) property that specifies which certificate to use when viewers use HTTPS to request objects\.

## Syntax<a name="w3ab2c21c14d307b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-viewercertificate-syntax.json"></a>

```
{
  "[AcmCertificateArn](#cfn-cloudfront-distribution-viewercertificate-acmcertificatearn)" : String,
  "[CloudFrontDefaultCertificate](#cfn-cloudfront-distribution-viewercertificate-cloudfrontdefaultcertificate)" : Boolean,
  "[IamCertificateId](#cfn-cloudfront-distribution-viewercertificate-iamcertificateid)" : String,
  "[MinimumProtocolVersion](#cfn-cloudfront-distribution-viewercertificate-minimumprotocolversion)" : String,
  "[SslSupportMethod](#cfn-cloudfront-distribution-viewercertificate-sslsupportmethod)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-viewercertificate-syntax.yaml"></a>

```
[AcmCertificateArn](#cfn-cloudfront-distribution-viewercertificate-acmcertificatearn): String
[CloudFrontDefaultCertificate](#cfn-cloudfront-distribution-viewercertificate-cloudfrontdefaultcertificate): Boolean
[IamCertificateId](#cfn-cloudfront-distribution-viewercertificate-iamcertificateid): String
[MinimumProtocolVersion](#cfn-cloudfront-distribution-viewercertificate-minimumprotocolversion): String
[SslSupportMethod](#cfn-cloudfront-distribution-viewercertificate-sslsupportmethod): String
```

## Properties<a name="w3ab2c21c14d307b7"></a>

`AcmCertificateArn`  <a name="cfn-cloudfront-distribution-viewercertificate-acmcertificatearn"></a>
If you're using an alternate domain name, the Amazon Resource Name \(ARN\) of an AWS Certificate Manager \(ACM\) certificate\. Use the ACM service to provision and manage your certificates\. For more information, see the [AWS Certificate Manager User Guide](http://docs.aws.amazon.com/acm/latest/userguide/)\.  
Currently, you can specify only certificates that are in the US East \(N\. Virginia\) region\.
*Required*: Conditional\. You must specify one of the following properties: `AcmCertificateArn`, `CloudFrontDefaultCertificate`, or `IamCertificateId`\.  
*Type*: String

`CloudFrontDefaultCertificate`  <a name="cfn-cloudfront-distribution-viewercertificate-cloudfrontdefaultcertificate"></a>
Indicates whether to use the default certificate for your CloudFront domain name when viewers use HTTPS to request your content\.  
*Required*: Conditional\. You must specify one of the following properties: `AcmCertificateArn`, `CloudFrontDefaultCertificate`, or `IamCertificateId`\.  
*Type*: Boolean

`IamCertificateId`  <a name="cfn-cloudfront-distribution-viewercertificate-iamcertificateid"></a>
If you're using an alternate domain name, the ID of a server certificate that was purchased from a certificate authority\. This ID is the `ServerCertificateId` value, which AWS Identity and Access Management \(IAM\) returns when the certificate is added to the IAM certificate store, such as `ASCACKCEVSQ6CEXAMPLE1`\.  
*Required*: Conditional\. You must specify one of the following properties: `AcmCertificateArn`, `CloudFrontDefaultCertificate`, or `IamCertificateId`\.  
*Type*: String

`MinimumProtocolVersion`  <a name="cfn-cloudfront-distribution-viewercertificate-minimumprotocolversion"></a>
The minimum version of the SSL protocol that you want CloudFront to use for HTTPS connections\. CloudFront serves your objects only to browsers or devices that support at least the SSL version that you specify\. For valid values, see the `MinimumProtocolVersion` content for the [ViewerCertificate](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html) data type in the *Amazon CloudFront API Reference*\.  
AWS CloudFormation specifies `SSLv3` by default\. However, if you specify the `IamCertificateId` or `AcmCertificateArn` property and specify SNI only for the `SslSupportMethod` property, AWS CloudFormation specifies `TLSv1` for the minimum protocol version\.  
*Required*: No  
*Type*: String

`SslSupportMethod`  <a name="cfn-cloudfront-distribution-viewercertificate-sslsupportmethod"></a>
Specifies how CloudFront serves HTTPS requests\. For valid values, see the `SslSupportMethod` content for the [ViewerCertificate](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html) data type in the *Amazon CloudFront API Reference*\.  
*Required*: Conditional\. Required if you specified the `IamCertificateId` or `AcmCertificateArn` property\.  
*Type*: String