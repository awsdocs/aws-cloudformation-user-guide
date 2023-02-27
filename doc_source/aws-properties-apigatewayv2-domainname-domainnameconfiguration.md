# AWS::ApiGatewayV2::DomainName DomainNameConfiguration<a name="aws-properties-apigatewayv2-domainname-domainnameconfiguration"></a>

The `DomainNameConfiguration` property type specifies the configuration for a an API's domain name\.

`DomainNameConfiguration` is a property of the [AWS::ApiGatewayV2::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-domainname.html) resource\.

## Syntax<a name="aws-properties-apigatewayv2-domainname-domainnameconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-domainname-domainnameconfiguration-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-apigatewayv2-domainname-domainnameconfiguration-certificatearn)" : String,
  "[CertificateName](#cfn-apigatewayv2-domainname-domainnameconfiguration-certificatename)" : String,
  "[EndpointType](#cfn-apigatewayv2-domainname-domainnameconfiguration-endpointtype)" : String,
  "[OwnershipVerificationCertificateArn](#cfn-apigatewayv2-domainname-domainnameconfiguration-ownershipverificationcertificatearn)" : String,
  "[SecurityPolicy](#cfn-apigatewayv2-domainname-domainnameconfiguration-securitypolicy)" : String
}
```

### YAML<a name="aws-properties-apigatewayv2-domainname-domainnameconfiguration-syntax.yaml"></a>

```
  [CertificateArn](#cfn-apigatewayv2-domainname-domainnameconfiguration-certificatearn): String
  [CertificateName](#cfn-apigatewayv2-domainname-domainnameconfiguration-certificatename): String
  [EndpointType](#cfn-apigatewayv2-domainname-domainnameconfiguration-endpointtype): String
  [OwnershipVerificationCertificateArn](#cfn-apigatewayv2-domainname-domainnameconfiguration-ownershipverificationcertificatearn): String
  [SecurityPolicy](#cfn-apigatewayv2-domainname-domainnameconfiguration-securitypolicy): String
```

## Properties<a name="aws-properties-apigatewayv2-domainname-domainnameconfiguration-properties"></a>

`CertificateArn`  <a name="cfn-apigatewayv2-domainname-domainnameconfiguration-certificatearn"></a>
An AWS\-managed certificate that will be used by the edge\-optimized endpoint for this domain name\. AWS Certificate Manager is the only supported source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CertificateName`  <a name="cfn-apigatewayv2-domainname-domainnameconfiguration-certificatename"></a>
The user\-friendly name of the certificate that will be used by the edge\-optimized endpoint for this domain name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointType`  <a name="cfn-apigatewayv2-domainname-domainnameconfiguration-endpointtype"></a>
The endpoint type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OwnershipVerificationCertificateArn`  <a name="cfn-apigatewayv2-domainname-domainnameconfiguration-ownershipverificationcertificatearn"></a>
The Amazon resource name \(ARN\) for the public certificate issued by AWS Certificate Manager\. This ARN is used to validate custom domain ownership\. It's required only if you configure mutual TLS and use either an ACM\-imported or a private CA certificate ARN as the regionalCertificateArn\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityPolicy`  <a name="cfn-apigatewayv2-domainname-domainnameconfiguration-securitypolicy"></a>
The Transport Layer Security \(TLS\) version of the security policy for this domain name\. The valid values are `TLS_1_0` and `TLS_1_2`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigatewayv2-domainname-domainnameconfiguration--seealso"></a>
+ [DomainNameConfiguration](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/domainnames-domainname.html#domainnames-domainname-model-domainnameconfiguration) in the *Amazon API Gateway Version 2 API Reference*

