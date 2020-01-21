# AWS::CloudFront::Distribution ViewerCertificate<a name="aws-properties-cloudfront-distribution-viewercertificate"></a>

A complex type that specifies the following:
+ Whether you want viewers to use HTTP or HTTPS to request your objects\.
+ If you want viewers to use HTTPS, whether you're using an alternate domain name, such as `example.com`, or the CloudFront domain name for your distribution, such as `d111111abcdef8.cloudfront.net`\.
+ If you're using an alternate domain name, whether AWS Certificate Manager \(ACM\) provided the certificate, or you purchased a certificate from a third\-party certificate authority and imported it into ACM or uploaded it to the IAM certificate store\.

Specify only one of the following values: 
+  [ACMCertificateArn](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html#cloudfront-Type-ViewerCertificate-ACMCertificateArn) 
+  [IAMCertificateId](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html#cloudfront-Type-ViewerCertificate-IAMCertificateId) 
+  [CloudFrontDefaultCertificate](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html#cloudfront-Type-ViewerCertificate-CloudFrontDefaultCertificate) 

For more information, see [ Using Alternate Domain Names and HTTPS](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/SecureConnections.html#CNAMEsAndHTTPS) in the *Amazon CloudFront Developer Guide*\.

## Syntax<a name="aws-properties-cloudfront-distribution-viewercertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-cloudfront-distribution-viewercertificate-properties"></a>

`AcmCertificateArn`  <a name="cfn-cloudfront-distribution-viewercertificate-acmcertificatearn"></a>
If you want viewers to use HTTPS to request your objects and you're using an alternate domain name, you must choose the type of certificate that you want to use\. If ACM provided your certificate, specify the Amazon Resource Name \(ARN\) for the ACM certificate that you want to use for this distribution\. CloudFront only supports ACM certificates in the US East \(N\. Virginia\) Region \(us\-east\-1\)\.  
If you specify an ACM certificate ARN, you must also specify an SSL support method \(`sni-only` or `vip`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudFrontDefaultCertificate`  <a name="cfn-cloudfront-distribution-viewercertificate-cloudfrontdefaultcertificate"></a>
If you're using the CloudFront domain name for your distribution, such as `d111111abcdef8.cloudfront.net`, specify this value as `true`\.  
*Required*: Conditional  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamCertificateId`  <a name="cfn-cloudfront-distribution-viewercertificate-iamcertificateid"></a>
If you want viewers to use HTTPS to request your objects and you're using an alternate domain name, you must choose the type of certificate that you want to use\. If you purchased your certificate from a third\-party certificate authority and uploaded it to the IAM certificate store, specify the certificate ID that you want to use for this distribution\.  
If you specify a certificate ID, you must also specify an SSL support method \(`sni-only` or `vip`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumProtocolVersion`  <a name="cfn-cloudfront-distribution-viewercertificate-minimumprotocolversion"></a>
Specify the security policy that you want CloudFront to use for HTTPS connections\. A security policy determines two settings:  
+ The minimum SSL/TLS protocol that CloudFront uses to communicate with viewers\.
+ The cipher that CloudFront uses to encrypt the content that it returns to viewers\.
On the CloudFront console, this setting is called **Security Policy**\.
We recommend that you specify `TLSv1.1_2016` unless your viewers are using browsers or devices that do not support TLSv1\.1 or later\.  
When both of the following are true, you must specify `TLSv1` or later for the security policy:   
+ You're using a custom certificate; that is, you specified a value for `ACMCertificateArn` or for `IAMCertificateId`\.
+ You're using SNI; that is, you specified `sni-only` for `SSLSupportMethod`\.
If you specify `true` for `CloudFrontDefaultCertificate`, CloudFront automatically sets the security policy to `TLSv1` regardless of the value that you specify here\.  
For information about the relationship between the security policy that you choose and the protocols and ciphers that CloudFront uses to communicate with viewers, see [ Supported SSL/TLS Protocols and Ciphers for Communication Between Viewers and CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/secure-connections-supported-viewer-protocols-ciphers.html#secure-connections-supported-ciphers) in the *Amazon CloudFront Developer Guide*\.  
*Required*: Conditional  
*Type*: String  
*Allowed Values*: `SSLv3 | TLSv1 | TLSv1.1_2016 | TLSv1.2_2018 | TLSv1_2016`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslSupportMethod`  <a name="cfn-cloudfront-distribution-viewercertificate-sslsupportmethod"></a>
If you specify a value for [ACMCertificateArn](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html#cloudfront-Type-ViewerCertificate-ACMCertificateArn) or for [IAMCertificateId](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html#cloudfront-Type-ViewerCertificate-IAMCertificateId), you must also specify how you want CloudFront to serve HTTPS requests: using a method that works for browsers and clients released after 2010, or one that works for all clients\.  
+  `sni-only`: CloudFront can respond to HTTPS requests from viewers that support Server Name Indication \(SNI\)\. All modern browsers support SNI, but there are a few that don't\. For a current list of the browsers that support SNI, see the [Wikipedia entry Server Name Indication](http://en.wikipedia.org/wiki/Server_Name_Indication)\. To learn about options to explore if you have viewers with browsers that don't include SNI support, see [Choosing How CloudFront Serves HTTPS Requests](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cnames-https-dedicated-ip-or-sni.html) in the *Amazon CloudFront Developer Guide*\.
+  `vip`: CloudFront uses dedicated IP addresses for your content and can respond to HTTPS requests from any viewer\. However, there are additional monthly charges\. For details, including specific pricing information, see [Custom SSL options for Amazon CloudFront](http://aws.amazon.com/cloudfront/custom-ssl-domains/) on the AWS marketing site\.
Don't specify a value here if you specified `CloudFrontDefaultCertificate` as `true`\.  
For more information, see [Choosing How CloudFront Serves HTTPS Requests](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cnames-https-dedicated-ip-or-sni.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: Conditional  
*Type*: String  
*Allowed Values*: `sni-only | vip`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-cloudfront-distribution-viewercertificate--seealso"></a>
+  [ViewerCertificate](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_ViewerCertificate.html) in the *Amazon CloudFront API Reference* 