# AWS::ACMPCA::CertificateAuthority CrlConfiguration<a name="aws-properties-acmpca-certificateauthority-crlconfiguration"></a>

Contains configuration information for a certificate revocation list \(CRL\)\. Your private certificate authority \(CA\) creates base CRLs\. Delta CRLs are not supported\. You can enable CRLs for your new or an existing private CA by setting the **Enabled** parameter to `true`\. Your private CA writes CRLs to an S3 bucket that you specify in the **S3BucketName** parameter\. You can hide the name of your bucket by specifying a value for the **CustomCname** parameter\. Your private CA copies the CNAME or the S3 bucket name to the **CRL Distribution Points** extension of each certificate it issues\. Your S3 bucket policy must give write permission to AWS Private CA\. 

 AWS Private CA assets that are stored in Amazon S3 can be protected with encryption\. For more information, see [Encrypting Your CRLs](https://docs.aws.amazon.com/privateca/latest/userguide/PcaCreateCa.html#crl-encryption)\.

Your private CA uses the value in the **ExpirationInDays** parameter to calculate the **nextUpdate** field in the CRL\. The CRL is refreshed prior to a certificate's expiration date or when a certificate is revoked\. When a certificate is revoked, it appears in the CRL until the certificate expires, and then in one additional CRL after expiration, and it always appears in the audit report\.

A CRL is typically updated approximately 30 minutes after a certificate is revoked\. If for any reason a CRL update fails, AWS Private CA makes further attempts every 15 minutes\.

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

Certificate revocation lists created by AWS Private CA are DER\-encoded\. You can use the following OpenSSL command to list a CRL\.

 `openssl crl -inform DER -text -in crl_path -noout` 

For more information, see [Planning a certificate revocation list \(CRL\)](https://docs.aws.amazon.com/privateca/latest/userguide/crl-planning.html) in the * AWS Private Certificate Authority User Guide* 

## Syntax<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-syntax.json"></a>

```
{
  "[CustomCname](#cfn-acmpca-certificateauthority-crlconfiguration-customcname)" : String,
  "[Enabled](#cfn-acmpca-certificateauthority-crlconfiguration-enabled)" : Boolean,
  "[ExpirationInDays](#cfn-acmpca-certificateauthority-crlconfiguration-expirationindays)" : Integer,
  "[S3BucketName](#cfn-acmpca-certificateauthority-crlconfiguration-s3bucketname)" : String,
  "[S3ObjectAcl](#cfn-acmpca-certificateauthority-crlconfiguration-s3objectacl)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-syntax.yaml"></a>

```
  [CustomCname](#cfn-acmpca-certificateauthority-crlconfiguration-customcname): String
  [Enabled](#cfn-acmpca-certificateauthority-crlconfiguration-enabled): Boolean
  [ExpirationInDays](#cfn-acmpca-certificateauthority-crlconfiguration-expirationindays): Integer
  [S3BucketName](#cfn-acmpca-certificateauthority-crlconfiguration-s3bucketname): String
  [S3ObjectAcl](#cfn-acmpca-certificateauthority-crlconfiguration-s3objectacl): String
```

## Properties<a name="aws-properties-acmpca-certificateauthority-crlconfiguration-properties"></a>

`CustomCname`  <a name="cfn-acmpca-certificateauthority-crlconfiguration-customcname"></a>
Name inserted into the certificate **CRL Distribution Points** extension that enables the use of an alias for the CRL distribution point\. Use this value if you don't want the name of your S3 bucket to be public\.  
The content of a Canonical Name \(CNAME\) record must conform to [RFC2396](https://www.ietf.org/rfc/rfc2396.txt) restrictions on the use of special characters in URIs\. Additionally, the value of the CNAME must not include a protocol prefix such as "http://" or "https://"\.
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `253`  
*Pattern*: `^[-a-zA-Z0-9;/?:@&=+$,%_.!~*()']*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-acmpca-certificateauthority-crlconfiguration-enabled"></a>
Boolean value that specifies whether certificate revocation lists \(CRLs\) are enabled\. You can use this value to enable certificate revocation for a new CA when you call the `CreateCertificateAuthority` operation or for an existing CA when you call the `UpdateCertificateAuthority` operation\.  
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
Name of the S3 bucket that contains the CRL\. If you do not provide a value for the **CustomCname** argument, the name of your S3 bucket is placed into the **CRL Distribution Points** extension of the issued certificate\. You can change the name of your bucket by calling the [UpdateCertificateAuthority](https://docs.aws.amazon.com/privateca/latest/APIReference/API_UpdateCertificateAuthority.html) operation\. You must specify a [bucket policy](https://docs.aws.amazon.com/privateca/latest/userguide/PcaCreateCa.html#s3-policies) that allows AWS Private CA to write the CRL to your bucket\.  
The `S3BucketName` parameter must conform to the [S3 bucket naming rules](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html)\.
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Pattern*: `^[-a-zA-Z0-9._/]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ObjectAcl`  <a name="cfn-acmpca-certificateauthority-crlconfiguration-s3objectacl"></a>
Determines whether the CRL will be publicly readable or privately held in the CRL Amazon S3 bucket\. If you choose PUBLIC\_READ, the CRL will be accessible over the public internet\. If you choose BUCKET\_OWNER\_FULL\_CONTROL, only the owner of the CRL S3 bucket can access the CRL, and your PKI clients may need an alternative method of access\.  
If no value is specified, the default is PUBLIC\_READ\.  
*Note:* This default can cause CA creation to fail in some circumstances\. If you have have enabled the Block Public Access \(BPA\) feature in your S3 account, then you must specify the value of this parameter as `BUCKET_OWNER_FULL_CONTROL`, and not doing so results in an error\. If you have disabled BPA in S3, then you can specify either `BUCKET_OWNER_FULL_CONTROL` or `PUBLIC_READ` as the value\.  
For more information, see [Blocking public access to the S3 bucket](https://docs.aws.amazon.com/privateca/latest/userguide/PcaCreateCa.html#s3-bpa)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)