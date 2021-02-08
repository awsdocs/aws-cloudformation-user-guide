# AWS::ACMPCA::CertificateAuthority CrlConfiguration<a name="aws-properties-acmpca-certificateauthority-crlconfiguration"></a>

Contains configuration information for a certificate revocation list \(CRL\)\. Your private certificate authority \(CA\) creates base CRLs\. Delta CRLs are not supported\. You can enable CRLs for your new or an existing private CA by setting the **Enabled** parameter to `true`\. Your private CA writes CRLs to an S3 bucket that you specify in the **S3BucketName** parameter\. You can hide the name of your bucket by specifying a value for the **CustomCname** parameter\. Your private CA copies the CNAME or the S3 bucket name to the **CRL Distribution Points** extension of each certificate it issues\. Your S3 bucket policy must give write permission to ACM Private CA\. 

ACM Private CAA assets that are stored in Amazon S3 can be protected with encryption\. For more information, see [Encrypting Your CRLs](https://docs.aws.amazon.com/acm-pca/latest/userguide/PcaCreateCa.html#crl-encryption)\.

Your private CA uses the value in the **ExpirationInDays** parameter to calculate the **nextUpdate** field in the CRL\. The CRL is refreshed at 1/2 the age of next update or when a certificate is revoked\. When a certificate is revoked, it is recorded in the next CRL that is generated and in the next audit report\. Only time valid certificates are listed in the CRL\. Expired certificates are not included\. 

CRLs contain the following fields:
+  **Version**: The current version number defined in RFC 5280 is V2\. The integer value is 0x1\. 
+  **Signature Algorithm**: The name of the algorithm used to sign the CRL\.
+  **Issuer**: The X\.500 distinguished name of your private CA that issued the CRL\.
+  **Last Update**: The issue date and time of this CRL\.
+  **Next Update**: The day and time by which the next CRL will be issued\.
+  **Revoked Certificates**: List of revoked certificates\. Each list item contains the following information\.
  +  **Serial Number**: The serial number, in hexadecimal format, of the revoked certificate\.
  +  **Revocation Date**: Date and time the certificate was revoked\.
  +  **CRL Entry Extensions**: Optional extensions for the CRL entry\.
    +  **X509v3 CRL Reason Code**: Reason the certificate was revoked\.
+  **CRL Extensions**: Optional extensions for the CRL\.
  +  **X509v3 Authority Key Identifier**: Identifies the public key associated with the private key used to sign the certificate\.
  +  **X509v3 CRL Number:**: Decimal sequence number for the CRL\.
+  **Signature Algorithm**: Algorithm used by your private CA to sign the CRL\.
+  **Signature Value**: Signature computed over the CRL\.

Certificate revocation lists created by ACM Private CA are DER\-encoded\. You can use the following OpenSSL command to list a CRL\.

 `openssl crl -inform DER -text -in crl_path -noout` 

## Syntax<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-syntax.json"></a>

```
{
  "[CustomCname](#cfn-acmpca-certificateauthority-crlconfiguration-customcname)" : String,
  "[Enabled](#cfn-acmpca-certificateauthority-crlconfiguration-enabled)" : Boolean,
  "[ExpirationInDays](#cfn-acmpca-certificateauthority-crlconfiguration-expirationindays)" : Integer,
  "[S3BucketName](#cfn-acmpca-certificateauthority-crlconfiguration-s3bucketname)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-syntax.yaml"></a>

```
  [CustomCname](#cfn-acmpca-certificateauthority-crlconfiguration-customcname): String
  [Enabled](#cfn-acmpca-certificateauthority-crlconfiguration-enabled): Boolean
  [ExpirationInDays](#cfn-acmpca-certificateauthority-crlconfiguration-expirationindays): Integer
  [S3BucketName](#cfn-acmpca-certificateauthority-crlconfiguration-s3bucketname): String
```

## Properties<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-properties"></a>

`CustomCname`  <a name="cfn-acmpca-certificateauthority-crlconfiguration-customcname"></a>
Name inserted into the certificate **CRL Distribution Points** extension that enables the use of an alias for the CRL distribution point\. Use this value if you don't want the name of your S3 bucket to be public\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `253`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-acmpca-certificateauthority-crlconfiguration-enabled"></a>
Boolean value that specifies whether certificate revocation lists \(CRLs\) are enabled\. You can use this value to enable certificate revocation for a new CA when you call the [CreateCertificateAuthority](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_CreateCertificateAuthority.html) action or for an existing CA when you call the [UpdateCertificateAuthority](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_UpdateCertificateAuthority.html) action\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpirationInDays`  <a name="cfn-acmpca-certificateauthority-crlconfiguration-expirationindays"></a>
Validity period of the CRL in days\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `5000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketName`  <a name="cfn-acmpca-certificateauthority-crlconfiguration-s3bucketname"></a>
Name of the S3 bucket that contains the CRL\. If you do not provide a value for the **CustomCname** argument, the name of your S3 bucket is placed into the **CRL Distribution Points** extension of the issued certificate\. You can change the name of your bucket by calling the [UpdateCertificateAuthority](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_UpdateCertificateAuthority.html) action\. You must specify a bucket policy that allows ACM Private CA to write the CRL to your bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)