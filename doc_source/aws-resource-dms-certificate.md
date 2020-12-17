# AWS::DMS::Certificate<a name="aws-resource-dms-certificate"></a>

The `AWS::DMS::Certificate` resource creates an SSL certificate that encrypts connections between AWS DMS endpoints and the replication instance\.

## Syntax<a name="aws-resource-dms-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-certificate-syntax.json"></a>

```
{
  "Type" : "AWS::DMS::Certificate",
  "Properties" : {
      "[CertificateIdentifier](#cfn-dms-certificate-certificateidentifier)" : String,
      "[CertificatePem](#cfn-dms-certificate-certificatepem)" : String,
      "[CertificateWallet](#cfn-dms-certificate-certificatewallet)" : String
    }
}
```

### YAML<a name="aws-resource-dms-certificate-syntax.yaml"></a>

```
Type: AWS::DMS::Certificate
Properties: 
  [CertificateIdentifier](#cfn-dms-certificate-certificateidentifier): String
  [CertificatePem](#cfn-dms-certificate-certificatepem): String
  [CertificateWallet](#cfn-dms-certificate-certificatewallet): String
```

## Properties<a name="aws-resource-dms-certificate-properties"></a>

`CertificateIdentifier`  <a name="cfn-dms-certificate-certificateidentifier"></a>
A customer\-assigned name for the certificate\. Identifiers must begin with a letter and must contain only ASCII letters, digits, and hyphens\. They can't end with a hyphen or contain two consecutive hyphens\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificatePem`  <a name="cfn-dms-certificate-certificatepem"></a>
The contents of a `.pem` file, which contains an X\.509 certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateWallet`  <a name="cfn-dms-certificate-certificatewallet"></a>
The location of an imported Oracle Wallet certificate for use with SSL\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-dms-certificate-return-values"></a>

### Ref<a name="aws-resource-dms-certificate-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the certificate\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-dms-certificate--examples"></a>



### <a name="aws-resource-dms-certificate--examples--"></a>

#### JSON<a name="aws-resource-dms-certificate--examples----json"></a>

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

#### YAML<a name="aws-resource-dms-certificate--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: "Certificate test"
Resources: 
  BasicCertificate: 
    Properties: 
      CertificatePem: |-
          -----BEGIN CERTIFICATE-----
           MIID/DCCAuSgAwIBAgABCDEFgkqhkiG9w0BAQsFADCBijEXAMPLE1UEBhMCVVMx...mqfEEuC7uUoPofXdBp2ObQ==
           -----END CERTIFICATE-----
    Type: "AWS::DMS::Certificate"
```

## See also<a name="aws-resource-dms-certificate--seealso"></a>
+  [ImportCertificate](https://docs.aws.amazon.com/dms/latest/APIReference/API_ImportCertificate.html) in the *AWS Database Migration Service API Reference* 
+  [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) 

