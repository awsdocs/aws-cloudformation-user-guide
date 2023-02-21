# AWS::ACMPCA::CertificateAuthority CsrExtensions<a name="aws-properties-acmpca-certificateauthority-csrextensions"></a>

Describes the certificate extensions to be added to the certificate signing request \(CSR\)\.

## Syntax<a name="aws-properties-acmpca-certificateauthority-csrextensions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificateauthority-csrextensions-syntax.json"></a>

```
{
  "[KeyUsage](#cfn-acmpca-certificateauthority-csrextensions-keyusage)" : KeyUsage,
  "[SubjectInformationAccess](#cfn-acmpca-certificateauthority-csrextensions-subjectinformationaccess)" : [ AccessDescription, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificateauthority-csrextensions-syntax.yaml"></a>

```
  [KeyUsage](#cfn-acmpca-certificateauthority-csrextensions-keyusage): 
    KeyUsage
  [SubjectInformationAccess](#cfn-acmpca-certificateauthority-csrextensions-subjectinformationaccess): 
    - AccessDescription
```

## Properties<a name="aws-properties-acmpca-certificateauthority-csrextensions-properties"></a>

`KeyUsage`  <a name="cfn-acmpca-certificateauthority-csrextensions-keyusage"></a>
Indicates the purpose of the certificate and of the key contained in the certificate\.  
*Required*: No  
*Type*: [KeyUsage](aws-properties-acmpca-certificateauthority-keyusage.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubjectInformationAccess`  <a name="cfn-acmpca-certificateauthority-csrextensions-subjectinformationaccess"></a>
For CA certificates, provides a path to additional information pertaining to the CA, such as revocation and policy\. For more information, see [Subject Information Access](https://datatracker.ietf.org/doc/html/rfc5280#section-4.2.2.2) in RFC 5280\.  
*Required*: No  
*Type*: List of [AccessDescription](aws-properties-acmpca-certificateauthority-accessdescription.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)