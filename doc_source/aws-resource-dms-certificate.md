# AWS::DMS::Certificate<a name="aws-resource-dms-certificate"></a>

The `AWS::DMS::Certificate` resource creates an SSL certificate that encrypts connections between AWS DMS endpoints and the replication instance\.

**Topics**
+ [Syntax](#aws-resource-dms-certificate-syntax)
+ [Properties](#aws-resource-dms-certificate-properties)
+ [Return Value](#aws-resource-dms-certificate-properties-returnvalues)
+ [Example](#aws-resource-dms-certificate-examples)
+ [See Also](#w3ab2c21c10d348c15)

## Syntax<a name="aws-resource-dms-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-certificate-syntax.json"></a>

```
{
  "Type": "AWS::DMS::Certificate",
  "Properties": {
    "[CertificateIdentifier](#cfn-dms-certificate-certificateidentifier)": String,
    "[CertificatePem](#cfn-dms-certificate-certificatepem)": String,
    "[CertificateWallet](#cfn-dms-certificate-certificatewallet)": String
  }
}
```

### YAML<a name="aws-resource-dms-certificate-syntax.yaml"></a>

```
Type: "AWS::DMS::Certificate"
Properties:
  [CertificateIdentifier](#cfn-dms-certificate-certificateidentifier): String
  [CertificatePem](#cfn-dms-certificate-certificatepem): String
  [CertificateWallet](#cfn-dms-certificate-certificatewallet): String
```

## Properties<a name="aws-resource-dms-certificate-properties"></a>

`CertificateIdentifier`  <a name="cfn-dms-certificate-certificateidentifier"></a>
The customer\-assigned name of the certificate\. Valid characters are `A-z` and `0-9`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CertificatePem`  <a name="cfn-dms-certificate-certificatepem"></a>
The contents of the \.pem X\.509 certificate file for the certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CertificateWallet`  <a name="cfn-dms-certificate-certificatewallet"></a>
The location of the imported Oracle Wallet certificate for use with SSL\.  
*Required*: No  
*Type:* Base64\-encoded binary data object  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-resource-dms-certificate-properties-returnvalues"></a>

### Ref<a name="w3ab2c21c10d348c11b3"></a>

When you pass the certificate of an `AWS::DMS::Certificate` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the certificate\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-dms-certificate-examples"></a>

### JSON<a name="aws-resource-dms-certificate-example1.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Certificate test",
  "Resources": {
    "BasicCertificate": {
      "Type": "AWS::DMS::Certificate",
      "Properties": {
        "CertificatePem": "-----BEGIN CERTIFICATE-----\n MIID/DCCAuSgAwIBAgIBUDANBgkqhkiG9w0BAQsFADCBijELMAkGA1UEBhMCVVMx...mqfEEuC7uUoPofXdBp2ObQ==\n -----END CERTIFICATE-----\n"
      }
    }
  }
}
```

### YAML<a name="aws-resource-dms-certificate-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Certificate test
Resources:
  BasicCertificate:
    Type: 'AWS::DMS::Certificate'
    Properties:
      CertificatePem: |
        -----BEGIN CERTIFICATE-----
         MIID/DCCAuSgAwIBAgIBUDANBgkqhkiG9w0BAQsFADCBijELMAkGA1UEBhMCVVMx...mqfEEuC7uUoPofXdBp2ObQ==
         -----END CERTIFICATE-----
```

## See Also<a name="w3ab2c21c10d348c15"></a>
+ [ImportCertificate](http://docs.aws.amazon.com/dms/latest/APIReference/API_ImportCertificate.html) in the *AWS Database Migration Service API Reference*\.
+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)