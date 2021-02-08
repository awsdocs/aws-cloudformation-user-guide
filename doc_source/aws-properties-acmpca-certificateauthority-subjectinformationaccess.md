# AWS::ACMPCA::CertificateAuthority SubjectInformationAccess<a name="aws-properties-acmpca-certificateauthority-subjectinformationaccess"></a>

For CA certificates, provides a path to additional information pertaining to the CA, such as revocation and policy\. For more information, see [Subject Information Access](https://tools.ietf.org/html/rfc5280#section-4.2.2.2) in RFC 5280\.

## Syntax<a name="aws-properties-acmpca-certificateauthority-subjectinformationaccess-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificateauthority-subjectinformationaccess-syntax.json"></a>

```
{
  "[SubjectInformationAccess](#cfn-acmpca-certificateauthority-subjectinformationaccess-subjectinformationaccess)" : [ AccessDescription, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificateauthority-subjectinformationaccess-syntax.yaml"></a>

```
  [SubjectInformationAccess](#cfn-acmpca-certificateauthority-subjectinformationaccess-subjectinformationaccess): 
    - AccessDescription
```

## Properties<a name="aws-properties-acmpca-certificateauthority-subjectinformationaccess-properties"></a>

`SubjectInformationAccess`  <a name="cfn-acmpca-certificateauthority-subjectinformationaccess-subjectinformationaccess"></a>
One or more objects providing paths to additional information pertaining to the CA, such as revocation and policy\.  
*Required*: No  
*Type*: [List](#aws-properties-acmpca-certificateauthority-subjectinformationaccess) of [AccessDescription](aws-properties-acmpca-certificateauthority-accessdescription.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)