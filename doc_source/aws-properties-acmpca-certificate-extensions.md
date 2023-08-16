# AWS::ACMPCA::Certificate Extensions<a name="aws-properties-acmpca-certificate-extensions"></a>

Contains X\.509 extension information for a certificate\.

## Syntax<a name="aws-properties-acmpca-certificate-extensions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-extensions-syntax.json"></a>

```
{
  "[CertificatePolicies](#cfn-acmpca-certificate-extensions-certificatepolicies)" : [ PolicyInformation, ... ],
  "[CustomExtensions](#cfn-acmpca-certificate-extensions-customextensions)" : [ CustomExtension, ... ],
  "[ExtendedKeyUsage](#cfn-acmpca-certificate-extensions-extendedkeyusage)" : [ ExtendedKeyUsage, ... ],
  "[KeyUsage](#cfn-acmpca-certificate-extensions-keyusage)" : KeyUsage,
  "[SubjectAlternativeNames](#cfn-acmpca-certificate-extensions-subjectalternativenames)" : [ GeneralName, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificate-extensions-syntax.yaml"></a>

```
  [CertificatePolicies](#cfn-acmpca-certificate-extensions-certificatepolicies): 
    - PolicyInformation
  [CustomExtensions](#cfn-acmpca-certificate-extensions-customextensions): 
    - CustomExtension
  [ExtendedKeyUsage](#cfn-acmpca-certificate-extensions-extendedkeyusage): 
    - ExtendedKeyUsage
  [KeyUsage](#cfn-acmpca-certificate-extensions-keyusage): 
    KeyUsage
  [SubjectAlternativeNames](#cfn-acmpca-certificate-extensions-subjectalternativenames): 
    - GeneralName
```

## Properties<a name="aws-properties-acmpca-certificate-extensions-properties"></a>

`CertificatePolicies`  <a name="cfn-acmpca-certificate-extensions-certificatepolicies"></a>
Contains a sequence of one or more policy information terms, each of which consists of an object identifier \(OID\) and optional qualifiers\. For more information, see NIST's definition of [Object Identifier \(OID\)](https://csrc.nist.gov/glossary/term/Object_Identifier)\.  
In an end\-entity certificate, these terms indicate the policy under which the certificate was issued and the purposes for which it may be used\. In a CA certificate, these terms limit the set of policies for certification paths that include this certificate\.  
*Required*: No  
*Type*: List of [PolicyInformation](aws-properties-acmpca-certificate-policyinformation.md)  
*Maximum*: `20`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CustomExtensions`  <a name="cfn-acmpca-certificate-extensions-customextensions"></a>
  
Contains a sequence of one or more X\.509 extensions, each of which consists of an object identifier \(OID\), a base64\-encoded value, and the critical flag\. For more information, see the [Global OID reference database\.](https://oidref.com/2.5.29)   
*Required*: No  
*Type*: List of [CustomExtension](aws-properties-acmpca-certificate-customextension.md)  
*Maximum*: `20`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExtendedKeyUsage`  <a name="cfn-acmpca-certificate-extensions-extendedkeyusage"></a>
Specifies additional purposes for which the certified public key may be used other than basic purposes indicated in the `KeyUsage` extension\.  
*Required*: No  
*Type*: [List](aws-properties-acmpca-certificate-extendedkeyusage.md) of [ExtendedKeyUsage](aws-properties-acmpca-certificate-extendedkeyusage.md)  
*Maximum*: `20`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyUsage`  <a name="cfn-acmpca-certificate-extensions-keyusage"></a>
Defines one or more purposes for which the key contained in the certificate can be used\. Default value for each option is false\.   
*Required*: No  
*Type*: [KeyUsage](aws-properties-acmpca-certificate-keyusage.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubjectAlternativeNames`  <a name="cfn-acmpca-certificate-extensions-subjectalternativenames"></a>
The subject alternative name extension allows identities to be bound to the subject of the certificate\. These identities may be included in addition to or in place of the identity in the subject field of the certificate\.  
*Required*: No  
*Type*: List of [GeneralName](aws-properties-acmpca-certificate-generalname.md)  
*Maximum*: `20`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)