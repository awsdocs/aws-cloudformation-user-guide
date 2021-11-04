# AWS::ACMPCA::CertificateAuthority RevocationConfiguration<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration"></a>

Certificate revocation information used by the CreateCertificateAuthority and UpdateCertificateAuthority actions\. Your private certificate authority \(CA\) can configure Online Certificate Status Protocol \(OCSP\) support and/or maintain a certificate revocation list \(CRL\)\. OCSP returns validation information about certificates as requested by clients, and a CRL contains an updated list of certificates revoked by your CA\. For more information, see [RevokeCertificate](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_RevokeCertificate.html)\.

## Syntax<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-syntax.json"></a>

```
{
  "[CrlConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration-crlconfiguration)" : CrlConfiguration,
  "[OcspConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration-ocspconfiguration)" : OcspConfiguration
}
```

### YAML<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-syntax.yaml"></a>

```
  [CrlConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration-crlconfiguration): 
    CrlConfiguration
  [OcspConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration-ocspconfiguration): 
    OcspConfiguration
```

## Properties<a name="aws-properties-acmpca-certificateauthority-revocationconfiguration-properties"></a>

`CrlConfiguration`  <a name="cfn-acmpca-certificateauthority-revocationconfiguration-crlconfiguration"></a>
Configuration of the certificate revocation list \(CRL\), if any, maintained by your private CA\.  
*Required*: No  
*Type*: [CrlConfiguration](aws-properties-acmpca-certificateauthority-crlconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OcspConfiguration`  <a name="cfn-acmpca-certificateauthority-revocationconfiguration-ocspconfiguration"></a>
Configuration of Online Certificate Status Protocol \(OCSP\) support, if any, maintained by your private CA\.  
*Required*: No  
*Type*: [OcspConfiguration](aws-properties-acmpca-certificateauthority-ocspconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)