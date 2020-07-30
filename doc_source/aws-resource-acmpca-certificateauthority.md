# AWS::ACMPCA::CertificateAuthority<a name="aws-resource-acmpca-certificateauthority"></a>

Use the `AWS::ACMPCA::CertificateAuthority` resource to create a private CA\. Once the CA exists, you can use the `AWS::ACMPCA::Certificate` resource to issue a new CA certificate\. Alternatively, you can issue a CA certificate using an on\-premises CA, and then use the `AWS::ACMPCA::CertificateAuthorityActivation` resource to import the new CA certificate and activate the CA\.

**Note**  
Before removing a `AWS::ACMPCA::CertificateAuthority` resource from the CloudFormation stack, disable the affected CA\. Otherwise, the action will fail\. You can disable the CA by removing its associated `AWS::ACMPCA::CertificateAuthorityActivation` resource from CloudFormation\. 

## Syntax<a name="aws-resource-acmpca-certificateauthority-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-acmpca-certificateauthority-syntax.json"></a>

```
{
  "Type" : "AWS::ACMPCA::CertificateAuthority",
  "Properties" : {
      "[KeyAlgorithm](#cfn-acmpca-certificateauthority-keyalgorithm)" : String,
      "[RevocationConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration)" : RevocationConfiguration,
      "[SigningAlgorithm](#cfn-acmpca-certificateauthority-signingalgorithm)" : String,
      "[Subject](#cfn-acmpca-certificateauthority-subject)" : Subject,
      "[Tags](#cfn-acmpca-certificateauthority-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-acmpca-certificateauthority-type)" : String
    }
}
```

### YAML<a name="aws-resource-acmpca-certificateauthority-syntax.yaml"></a>

```
Type: AWS::ACMPCA::CertificateAuthority
Properties: 
  [KeyAlgorithm](#cfn-acmpca-certificateauthority-keyalgorithm): String
  [RevocationConfiguration](#cfn-acmpca-certificateauthority-revocationconfiguration): 
    RevocationConfiguration
  [SigningAlgorithm](#cfn-acmpca-certificateauthority-signingalgorithm): String
  [Subject](#cfn-acmpca-certificateauthority-subject): 
    Subject
  [Tags](#cfn-acmpca-certificateauthority-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-acmpca-certificateauthority-type): String
```

## Properties<a name="aws-resource-acmpca-certificateauthority-properties"></a>

`KeyAlgorithm`  <a name="cfn-acmpca-certificateauthority-keyalgorithm"></a>
Type of the public key algorithm and size, in bits, of the key pair that your CA creates when it issues a certificate\. When you create a subordinate CA, you must use a key algorithm supported by the parent CA\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EC_prime256v1 | EC_secp384r1 | RSA_2048 | RSA_4096`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RevocationConfiguration`  <a name="cfn-acmpca-certificateauthority-revocationconfiguration"></a>
Information about the certificate revocation list \(CRL\) created and maintained by your private CA\. Certificate revocation information used by the CreateCertificateAuthority and UpdateCertificateAuthority actions\. Your certificate authority can create and maintain a certificate revocation list \(CRL\)\. A CRL contains information about certificates that have been revoked\.  
*Required*: No  
*Type*: [RevocationConfiguration](aws-properties-acmpca-certificateauthority-revocationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SigningAlgorithm`  <a name="cfn-acmpca-certificateauthority-signingalgorithm"></a>
Name of the algorithm your private CA uses to sign certificate requests\.  
This parameter should not be confused with the `SigningAlgorithm` parameter used to sign certificates when they are issued\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SHA256WITHECDSA | SHA256WITHRSA | SHA384WITHECDSA | SHA384WITHRSA | SHA512WITHECDSA | SHA512WITHRSA`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subject`  <a name="cfn-acmpca-certificateauthority-subject"></a>
Structure that contains X\.500 distinguished name information for your private CA\.  
*Required*: Yes  
*Type*: [Subject](aws-properties-acmpca-certificateauthority-subject.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-acmpca-certificateauthority-tags"></a>
Key\-value pairs that will be attached to the new private CA\. You can associate up to 50 tags with a private CA\. For information using tags with IAM to manage permissions, see [Controlling Access Using IAM Tags](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_iam-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-acmpca-certificateauthority-type"></a>
Type of your private CA\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ROOT | SUBORDINATE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-acmpca-certificateauthority-return-values"></a>

### Ref<a name="aws-resource-acmpca-certificateauthority-return-values-ref"></a>

The Amazon Resource Name \(ARN\) of the certificate authority\.

### Fn::GetAtt<a name="aws-resource-acmpca-certificateauthority-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-acmpca-certificateauthority-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the private CA that issued the certificate\.

`CertificateSigningRequest`  <a name="CertificateSigningRequest-fn::getatt"></a>
The Base64 PEM\-encoded certificate signing request \(CSR\) for your certificate authority certificate\.

## Examples<a name="aws-resource-acmpca-certificateauthority--examples"></a>

The following example of a CloudFormation template sets up a CA hierarchy\. The example illustrates the use of `AWS::ACMPCA::Certificate`, `AWS::ACMPCA::CertificateAuthority`, and `AWS::ACMPCA::CertificateAuthorityActivation` resources\. 

### Declaring a Private CA Hierarchy<a name="aws-resource-acmpca-certificateauthority--examples--Declaring_a_Private_CA_Hierarchy"></a>

#### JSON<a name="aws-resource-acmpca-certificateauthority--examples--Declaring_a_Private_CA_Hierarchy--json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Description":"Cloudformation template to setup CA.",
   "Resources":{
      "RootCA":{
         "Type":"AWS::ACMPCA::CertificateAuthority",
         "Properties":{
            "Type":"ROOT",
            "KeyAlgorithm":"RSA_2048",
            "SigningAlgorithm":"SHA256WITHRSA",
            "Subject":{
               "Country":"US",
               "Organization":"string",
               "OrganizationalUnit":"string",
               "DistinguishedNameQualifier":"string",
               "State":"string",
               "CommonName":"123",
               "SerialNumber":"string",
               "Locality":"string",
               "Title":"string",
               "Surname":"string",
               "GivenName":"string",
               "Initials":"DG",
               "Pseudonym":"string",
               "GenerationQualifier":"DBG"
            },
            "RevocationConfiguration":{
               "CrlConfiguration":{
                  "Enabled":false
               }
            }
         }
      },
      "RootCACertificate":{
         "Type":"AWS::ACMPCA::Certificate",
         "Properties":{
            "CertificateAuthorityArn":{
               "Ref":"RootCA"
            },
            "CertificateSigningRequest":{
               "Fn::GetAtt":[
                  "RootCA",
                  "CertificateSigningRequest"
               ]
            },
            "SigningAlgorithm":"SHA256WITHRSA",
            "TemplateArn":"arn:aws:acm-pca:::template/RootCACertificate/V1",
            "Validity":{
               "Type":"DAYS",
               "Value":100
            }
         }
      },
      "RootCAActivation":{
         "Type":"AWS::ACMPCA::CertificateAuthorityActivation",
         "Properties":{
            "CertificateAuthorityArn":{
               "Ref":"RootCA"
            },
            "Certificate":{
               "Fn::GetAtt":[
                  "RootCACertificate",
                  "Certificate"
               ]
            },
            "Status":"ACTIVE"
         }
      },
      "SubordinateCAOne":{
         "Type":"AWS::ACMPCA::CertificateAuthority",
         "Properties":{
            "Type":"SUBORDINATE",
            "KeyAlgorithm":"RSA_2048",
            "SigningAlgorithm":"SHA256WITHRSA",
            "Subject":{
               "Country":"US",
               "Organization":"string",
               "OrganizationalUnit":"string",
               "DistinguishedNameQualifier":"string",
               "State":"string",
               "CommonName":"Sub1",
               "SerialNumber":"string",
               "Locality":"string",
               "Title":"string",
               "Surname":"string",
               "GivenName":"string",
               "Initials":"DG",
               "Pseudonym":"string",
               "GenerationQualifier":"DBG"
            },
            "RevocationConfiguration":{

            },
            "Tags":[

            ]
         }
      },
      "SubordinateCAOneCACertificate":{
         "DependsOn":"RootCAActivation",
         "Type":"AWS::ACMPCA::Certificate",
         "Properties":{
            "CertificateAuthorityArn":{
               "Ref":"RootCA"
            },
            "CertificateSigningRequest":{
               "Fn::GetAtt":[
                  "SubordinateCAOne",
                  "CertificateSigningRequest"
               ]
            },
            "SigningAlgorithm":"SHA256WITHRSA",
            "TemplateArn":"arn:aws:acm-pca:::template/SubordinateCACertificate_PathLen3/V1",
            "Validity":{
               "Type":"DAYS",
               "Value":90
            }
         }
      },
      "SubordinateCAOneActivation":{
         "Type":"AWS::ACMPCA::CertificateAuthorityActivation",
         "Properties":{
            "CertificateAuthorityArn":{
               "Ref":"SubordinateCAOne"
            },
            "Certificate":{
               "Fn::GetAtt":[
                  "SubordinateCAOneCACertificate",
                  "Certificate"
               ]
            },
            "CertificateChain":{
               "Fn::GetAtt":[
                  "RootCAActivation",
                  "CompleteCertificateChain"
               ]
            },
            "Status":"ACTIVE"
         }
      },
      "SubordinateCATwo":{
         "Type":"AWS::ACMPCA::CertificateAuthority",
         "Properties":{
            "Type":"SUBORDINATE",
            "KeyAlgorithm":"RSA_2048",
            "SigningAlgorithm":"SHA256WITHRSA",
            "Subject":{
               "Country":"US",
               "Organization":"string",
               "OrganizationalUnit":"string",
               "DistinguishedNameQualifier":"string",
               "State":"string",
               "SerialNumber":"string",
               "Locality":"string",
               "Title":"string",
               "Surname":"string",
               "GivenName":"string",
               "Initials":"DG",
               "Pseudonym":"string",
               "GenerationQualifier":"DBG"
            },
            "Tags":[
               {
                  "Key":"Key1",
                  "Value":"Value1"
               },
               {
                  "Key":"Key2",
                  "Value":"Value2"
               }
            ]
         }
      },
      "SubordinateCATwoCACertificate":{
         "DependsOn":"SubordinateCAOneActivation",
         "Type":"AWS::ACMPCA::Certificate",
         "Properties":{
            "CertificateAuthorityArn":{
               "Ref":"SubordinateCAOne"
            },
            "CertificateSigningRequest":{
               "Fn::GetAtt":[
                  "SubordinateCATwo",
                  "CertificateSigningRequest"
               ]
            },
            "SigningAlgorithm":"SHA256WITHRSA",
            "TemplateArn":"arn:aws:acm-pca:::template/SubordinateCACertificate_PathLen2/V1",
            "Validity":{
               "Type":"DAYS",
               "Value":80
            }
         }
      },
      "SubordinateCATwoActivation":{
         "Type":"AWS::ACMPCA::CertificateAuthorityActivation",
         "Properties":{
            "CertificateAuthorityArn":{
               "Ref":"SubordinateCATwo"
            },
            "Certificate":{
               "Fn::GetAtt":[
                  "SubordinateCATwoCACertificate",
                  "Certificate"
               ]
            },
            "CertificateChain":{
               "Fn::GetAtt":[
                  "SubordinateCAOneActivation",
                  "CompleteCertificateChain"
               ]
            }
         }
      },
      "EndEntityCertificate":{
         "DependsOn":"SubordinateCATwoActivation",
         "Type":"AWS::ACMPCA::Certificate",
         "Properties":{
            "CertificateAuthorityArn":{
               "Ref":"SubordinateCATwo"
            },
            "CertificateSigningRequest":{
               "Fn::Join":[
                  "\n",
                  [
                     "-----BEGIN CERTIFICATE REQUEST-----",
                     "MIICvDCCAaQCAQAwdzELMAkGA1UEBhMCVVMxDTALBgNVBAgMBFV0YWgxDzANBgNV",
                     "BAcMBkxpbmRvbjEWMBQGA1UECgwNRGlnaUNlcnQgSW5jLjERMA8GA1UECwwIRGln",
                     "aUNlcnQxHTAbBgNVBAMMFGV4YW1wbGUuZGlnaWNlcnQuY29tMIIBIjANBgkqhkiG",
                     "9w0BAQEFAAOCAQ8AMIIBCgKCAQEA8+To7d+2kPWeBv/orU3LVbJwDrSQbeKamCmo",
                     "wp5bqDxIwV20zqRb7APUOKYoVEFFOEQs6T6gImnIolhbiH6m4zgZ/CPvWBOkZc+c",
                     "1Po2EmvBz+AD5sBdT5kzGQA6NbWyZGldxRthNLOs1efOhdnWFuhI162qmcflgpiI",
                     "WDuwq4C9f+YkeJhNn9dF5+owm8cOQmDrV8NNdiTqin8q3qYAHHJRW28glJUCZkTZ",
                     "wIaSR6crBQ8TbYNE0dc+Caa3DOIkz1EOsHWzTx+n0zKfqcbgXi4DJx+C1bjptYPR",
                     "BPZL8DAeWuA8ebudVT44yEp82G96/Ggcf7F33xMxe0yc+Xa6owIDAQABoAAwDQYJ",
                     "KoZIhvcNAQEFBQADggEBAB0kcrFccSmFDmxox0Ne01UIqSsDqHgL+XmHTXJwre6D",
                     "hJSZwbvEtOK0G3+dr4Fs11WuUNt5qcLsx5a8uk4G6AKHMzuhLsJ7XZjgmQXGECpY",
                     "Q4mC3yT3ZoCGpIXbw+iP3lmEEXgaQL0Tx5LFl/okKbKYwIqNiyKWOMj7ZR/wxWg/",
                     "ZDGRs55xuoeLDJ/ZRFf9bI+IaCUd1YrfYcHIl3G87Av+r49YVwqRDT0VDV7uLgqn",
                     "29XI1PpVUNCPQGn9p/eX6Qo7vpDaPybRtA2R7XLKjQaF9oXWeCUqy1hvJac9QFO2",
                     "97Ob1alpHPoZ7mWiEuJwjBPii6a9M9G30nUo39lBi1w=",
                     "-----END CERTIFICATE REQUEST-----"
                  ]
               ]
            },
            "SigningAlgorithm":"SHA256WITHRSA",
            "Validity":{
               "Type":"DAYS",
               "Value":70
            }
         }
      }
   },
   "Outputs":{
      "CompleteCertificateChain":{
         "Value":{
            "Fn::GetAtt":[
               "SubordinateCATwoActivation",
               "CompleteCertificateChain"
            ]
         }
      },
      "CertificateArn":{
         "Value":{
            "Fn::GetAtt":[
               "EndEntityCertificate",
               "Arn"
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-acmpca-certificateauthority--examples--Declaring_a_Private_CA_Hierarchy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Cloudformation template to setup CA.
Resources:
  RootCA:
    Type: 'AWS::ACMPCA::CertificateAuthority'
    Properties:
      Type: ROOT
      KeyAlgorithm: RSA_2048
      SigningAlgorithm: SHA256WITHRSA
      Subject:
        Country: US
        Organization: string
        OrganizationalUnit: string
        DistinguishedNameQualifier: string
        State: string
        CommonName: '123'
        SerialNumber: string
        Locality: string
        Title: string
        Surname: string
        GivenName: string
        Initials: DG
        Pseudonym: string
        GenerationQualifier: DBG
      RevocationConfiguration:
        CrlConfiguration:
          Enabled: false
  RootCACertificate:
    Type: 'AWS::ACMPCA::Certificate'
    Properties:
      CertificateAuthorityArn: !Ref RootCA
      CertificateSigningRequest: !GetAtt 
        - RootCA
        - CertificateSigningRequest
      SigningAlgorithm: SHA256WITHRSA
      TemplateArn: 'arn:aws:acm-pca:::template/RootCACertificate/V1'
      Validity:
        Type: DAYS
        Value: 100
  RootCAActivation:
    Type: 'AWS::ACMPCA::CertificateAuthorityActivation'
    Properties:
      CertificateAuthorityArn: !Ref RootCA
      Certificate: !GetAtt 
        - RootCACertificate
        - Certificate
      Status: ACTIVE
  SubordinateCAOne:
    Type: 'AWS::ACMPCA::CertificateAuthority'
    Properties:
      Type: SUBORDINATE
      KeyAlgorithm: RSA_2048
      SigningAlgorithm: SHA256WITHRSA
      Subject:
        Country: US
        Organization: string
        OrganizationalUnit: string
        DistinguishedNameQualifier: string
        State: string
        CommonName: Sub1
        SerialNumber: string
        Locality: string
        Title: string
        Surname: string
        GivenName: string
        Initials: DG
        Pseudonym: string
        GenerationQualifier: DBG
      RevocationConfiguration: {}
      Tags: []
  SubordinateCAOneCACertificate:
    DependsOn: RootCAActivation
    Type: 'AWS::ACMPCA::Certificate'
    Properties:
      CertificateAuthorityArn: !Ref RootCA
      CertificateSigningRequest: !GetAtt 
        - SubordinateCAOne
        - CertificateSigningRequest
      SigningAlgorithm: SHA256WITHRSA
      TemplateArn: 'arn:aws:acm-pca:::template/SubordinateCACertificate_PathLen3/V1'
      Validity:
        Type: DAYS
        Value: 90
  SubordinateCAOneActivation:
    Type: 'AWS::ACMPCA::CertificateAuthorityActivation'
    Properties:
      CertificateAuthorityArn: !Ref SubordinateCAOne
      Certificate: !GetAtt 
        - SubordinateCAOneCACertificate
        - Certificate
      CertificateChain: !GetAtt 
        - RootCAActivation
        - CompleteCertificateChain
      Status: ACTIVE
  SubordinateCATwo:
    Type: 'AWS::ACMPCA::CertificateAuthority'
    Properties:
      Type: SUBORDINATE
      KeyAlgorithm: RSA_2048
      SigningAlgorithm: SHA256WITHRSA
      Subject:
        Country: US
        Organization: string
        OrganizationalUnit: string
        DistinguishedNameQualifier: string
        State: string
        SerialNumber: string
        Locality: string
        Title: string
        Surname: string
        GivenName: string
        Initials: DG
        Pseudonym: string
        GenerationQualifier: DBG
      Tags:
        - Key: Key1
          Value: Value1
        - Key: Key2
          Value: Value2
  SubordinateCATwoCACertificate:
    DependsOn: SubordinateCAOneActivation
    Type: 'AWS::ACMPCA::Certificate'
    Properties:
      CertificateAuthorityArn: !Ref SubordinateCAOne
      CertificateSigningRequest: !GetAtt 
        - SubordinateCATwo
        - CertificateSigningRequest
      SigningAlgorithm: SHA256WITHRSA
      TemplateArn: 'arn:aws:acm-pca:::template/SubordinateCACertificate_PathLen2/V1'
      Validity:
        Type: DAYS
        Value: 80
  SubordinateCATwoActivation:
    Type: 'AWS::ACMPCA::CertificateAuthorityActivation'
    Properties:
      CertificateAuthorityArn: !Ref SubordinateCATwo
      Certificate: !GetAtt 
        - SubordinateCATwoCACertificate
        - Certificate
      CertificateChain: !GetAtt 
        - SubordinateCAOneActivation
        - CompleteCertificateChain
  EndEntityCertificate:
    DependsOn: SubordinateCATwoActivation
    Type: 'AWS::ACMPCA::Certificate'
    Properties:
      CertificateAuthorityArn: !Ref SubordinateCATwo
      CertificateSigningRequest: !Join 
        - |+
 
        - - '-----BEGIN CERTIFICATE REQUEST-----'
          - MIICvDCCAaQCAQAwdzELMAkGA1UEBhMCVVMxDTALBgNVBAgMBFV0YWgxDzANBgNV
          - BAcMBkxpbmRvbjEWMBQGA1UECgwNRGlnaUNlcnQgSW5jLjERMA8GA1UECwwIRGln
          - aUNlcnQxHTAbBgNVBAMMFGV4YW1wbGUuZGlnaWNlcnQuY29tMIIBIjANBgkqhkiG
          - 9w0BAQEFAAOCAQ8AMIIBCgKCAQEA8+To7d+2kPWeBv/orU3LVbJwDrSQbeKamCmo
          - wp5bqDxIwV20zqRb7APUOKYoVEFFOEQs6T6gImnIolhbiH6m4zgZ/CPvWBOkZc+c
          - 1Po2EmvBz+AD5sBdT5kzGQA6NbWyZGldxRthNLOs1efOhdnWFuhI162qmcflgpiI
          - WDuwq4C9f+YkeJhNn9dF5+owm8cOQmDrV8NNdiTqin8q3qYAHHJRW28glJUCZkTZ
          - wIaSR6crBQ8TbYNE0dc+Caa3DOIkz1EOsHWzTx+n0zKfqcbgXi4DJx+C1bjptYPR
          - BPZL8DAeWuA8ebudVT44yEp82G96/Ggcf7F33xMxe0yc+Xa6owIDAQABoAAwDQYJ
          - KoZIhvcNAQEFBQADggEBAB0kcrFccSmFDmxox0Ne01UIqSsDqHgL+XmHTXJwre6D
          - hJSZwbvEtOK0G3+dr4Fs11WuUNt5qcLsx5a8uk4G6AKHMzuhLsJ7XZjgmQXGECpY
          - Q4mC3yT3ZoCGpIXbw+iP3lmEEXgaQL0Tx5LFl/okKbKYwIqNiyKWOMj7ZR/wxWg/
          - ZDGRs55xuoeLDJ/ZRFf9bI+IaCUd1YrfYcHIl3G87Av+r49YVwqRDT0VDV7uLgqn
          - 29XI1PpVUNCPQGn9p/eX6Qo7vpDaPybRtA2R7XLKjQaF9oXWeCUqy1hvJac9QFO2
          - 97Ob1alpHPoZ7mWiEuJwjBPii6a9M9G30nUo39lBi1w=
          - '-----END CERTIFICATE REQUEST-----'
      SigningAlgorithm: SHA256WITHRSA
      Validity:
        Type: DAYS
        Value: 70
Outputs:
  CompleteCertificateChain:
    Value: !GetAtt 
      - SubordinateCATwoActivation
      - CompleteCertificateChain
  CertificateArn:
    Value: !GetAtt 
      - EndEntityCertificate
      - Arn
```