# AWS::ACMPCA::Certificate<a name="aws-resource-acmpca-certificate"></a>

The `AWS::ACMPCA::Certificate` resource is used to issue a certificate using your private certificate authority\. For more information, see the [IssueCertificate](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_IssueCertificate.html) action\.

## Syntax<a name="aws-resource-acmpca-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-acmpca-certificate-syntax.json"></a>

```
{
  "Type" : "AWS::ACMPCA::Certificate",
  "Properties" : {
      "[CertificateAuthorityArn](#cfn-acmpca-certificate-certificateauthorityarn)" : String,
      "[CertificateSigningRequest](#cfn-acmpca-certificate-certificatesigningrequest)" : String,
      "[SigningAlgorithm](#cfn-acmpca-certificate-signingalgorithm)" : String,
      "[TemplateArn](#cfn-acmpca-certificate-templatearn)" : String,
      "[Validity](#cfn-acmpca-certificate-validity)" : Validity
    }
}
```

### YAML<a name="aws-resource-acmpca-certificate-syntax.yaml"></a>

```
Type: AWS::ACMPCA::Certificate
Properties: 
  [CertificateAuthorityArn](#cfn-acmpca-certificate-certificateauthorityarn): String
  [CertificateSigningRequest](#cfn-acmpca-certificate-certificatesigningrequest): String
  [SigningAlgorithm](#cfn-acmpca-certificate-signingalgorithm): String
  [TemplateArn](#cfn-acmpca-certificate-templatearn): String
  [Validity](#cfn-acmpca-certificate-validity): 
    Validity
```

## Properties<a name="aws-resource-acmpca-certificate-properties"></a>

`CertificateAuthorityArn`  <a name="cfn-acmpca-certificate-certificateauthorityarn"></a>
The Amazon Resource Name \(ARN\) for the private CA used to issue the certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateSigningRequest`  <a name="cfn-acmpca-certificate-certificatesigningrequest"></a>
The certificate signing request \(CSR\) for the certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SigningAlgorithm`  <a name="cfn-acmpca-certificate-signingalgorithm"></a>
The name of the algorithm that will be used to sign the certificate to be issued\.   
This parameter should not be confused with the `SigningAlgorithm` parameter used to sign a CSR\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SHA256WITHECDSA | SHA256WITHRSA | SHA384WITHECDSA | SHA384WITHRSA | SHA512WITHECDSA | SHA512WITHRSA`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TemplateArn`  <a name="cfn-acmpca-certificate-templatearn"></a>
Specifies a custom configuration template to use when issuing a certificate\. If this parameter is not provided, ACM Private CA defaults to the `EndEntityCertificate/V1` template\. For more information about ACM Private CA templates, see [Using Templates](https://docs.aws.amazon.com/acm-pca/latest/userguide/UsingTemplates.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Validity`  <a name="cfn-acmpca-certificate-validity"></a>
The period of time during which the certificate will be valid\.  
*Required*: Yes  
*Type*: [Validity](aws-properties-acmpca-certificate-validity.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-acmpca-certificate-return-values"></a>

### Ref<a name="aws-resource-acmpca-certificate-return-values-ref"></a>

This reference should not be used in CloudFormation templates\. Instead, use `AWS::ACMPCA::Certificate.Arn` to identify a certificate, and use `AWS::ACMPCA::Certificate.CertificateAuthorityArn` to identify a certificate authority\.

### Fn::GetAtt<a name="aws-resource-acmpca-certificate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-acmpca-certificate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the issued certificate\.

`Certificate`  <a name="Certificate-fn::getatt"></a>
The issued Base64 PEM\-encoded certificate\.