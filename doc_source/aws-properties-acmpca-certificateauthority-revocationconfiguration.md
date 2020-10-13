# AWS::ACMPCA::CertificateAuthority RevocationConfiguration<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration"></a>

Certificate revocation information used by the [CreateCertificateAuthority](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_CreateCertificateAuthority.html) and [UpdateCertificateAuthority](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_UpdateCertificateAuthority.html) actions\. Your private certificate authority \(CA\) can create and maintain a certificate revocation list \(CRL\)\. A CRL contains information about certificates revoked by your CA\. For more information, see [RevokeCertificate](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_RevokeCertificate.html)\.

## Syntax<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-syntax.json"></a>

```
{
  "[CrlConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration-crlconfiguration)" : CrlConfiguration
}
```

### YAML<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-syntax.yaml"></a>

```
  [CrlConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration-crlconfiguration): 
    CrlConfiguration
```

## Properties<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-properties"></a>

`CrlConfiguration`  <a name="cfn-acmpca-certificateauthority-revocationconfiguration-crlconfiguration"></a>
Configuration of the certificate revocation list \(CRL\), if any, maintained by your private CA\.  
*Required*: No  
*Type*: [CrlConfiguration](aws-properties-acmpca-certificateauthority-crlconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)