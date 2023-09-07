# AWS::PCAConnectorAD::Template EnrollmentFlagsV3<a name="aws-properties-pcaconnectorad-template-enrollmentflagsv3"></a>

Template configurations for v3 template schema\.

## Syntax<a name="aws-properties-pcaconnectorad-template-enrollmentflagsv3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-enrollmentflagsv3-syntax.json"></a>

```
{
  "[EnableKeyReuseOnNtTokenKeysetStorageFull](#cfn-pcaconnectorad-template-enrollmentflagsv3-enablekeyreuseonnttokenkeysetstoragefull)" : Boolean,
  "[IncludeSymmetricAlgorithms](#cfn-pcaconnectorad-template-enrollmentflagsv3-includesymmetricalgorithms)" : Boolean,
  "[NoSecurityExtension](#cfn-pcaconnectorad-template-enrollmentflagsv3-nosecurityextension)" : Boolean,
  "[RemoveInvalidCertificateFromPersonalStore](#cfn-pcaconnectorad-template-enrollmentflagsv3-removeinvalidcertificatefrompersonalstore)" : Boolean,
  "[UserInteractionRequired](#cfn-pcaconnectorad-template-enrollmentflagsv3-userinteractionrequired)" : Boolean
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-enrollmentflagsv3-syntax.yaml"></a>

```
  [EnableKeyReuseOnNtTokenKeysetStorageFull](#cfn-pcaconnectorad-template-enrollmentflagsv3-enablekeyreuseonnttokenkeysetstoragefull): Boolean
  [IncludeSymmetricAlgorithms](#cfn-pcaconnectorad-template-enrollmentflagsv3-includesymmetricalgorithms): Boolean
  [NoSecurityExtension](#cfn-pcaconnectorad-template-enrollmentflagsv3-nosecurityextension): Boolean
  [RemoveInvalidCertificateFromPersonalStore](#cfn-pcaconnectorad-template-enrollmentflagsv3-removeinvalidcertificatefrompersonalstore): Boolean
  [UserInteractionRequired](#cfn-pcaconnectorad-template-enrollmentflagsv3-userinteractionrequired): Boolean
```

## Properties<a name="aws-properties-pcaconnectorad-template-enrollmentflagsv3-properties"></a>

`EnableKeyReuseOnNtTokenKeysetStorageFull`  <a name="cfn-pcaconnectorad-template-enrollmentflagsv3-enablekeyreuseonnttokenkeysetstoragefull"></a>
Allow renewal using the same key\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeSymmetricAlgorithms`  <a name="cfn-pcaconnectorad-template-enrollmentflagsv3-includesymmetricalgorithms"></a>
Include symmetric algorithms allowed by the subject\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoSecurityExtension`  <a name="cfn-pcaconnectorad-template-enrollmentflagsv3-nosecurityextension"></a>
This flag instructs the CA to not include the security extension szOID\_NTDS\_CA\_SECURITY\_EXT \(OID:1\.3\.6\.1\.4\.1\.311\.25\.2\), as specified in \[MS\-WCCE\] sections 2\.2\.2\.7\.7\.4 and 3\.2\.2\.6\.2\.1\.4\.5\.9, in the issued certificate\. This addresses a Windows Kerberos elevation\-of\-privilege vulnerability\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveInvalidCertificateFromPersonalStore`  <a name="cfn-pcaconnectorad-template-enrollmentflagsv3-removeinvalidcertificatefrompersonalstore"></a>
Delete expired or revoked certificates instead of archiving them\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserInteractionRequired`  <a name="cfn-pcaconnectorad-template-enrollmentflagsv3-userinteractionrequired"></a>
Require user interaction when the subject is enrolled and the private key associated with the certificate is used\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)