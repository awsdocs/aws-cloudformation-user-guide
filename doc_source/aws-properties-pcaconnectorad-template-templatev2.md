# AWS::PCAConnectorAD::Template TemplateV2<a name="aws-properties-pcaconnectorad-template-templatev2"></a>

v2 template schema that uses Legacy Cryptographic Providers\.

## Syntax<a name="aws-properties-pcaconnectorad-template-templatev2-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-templatev2-syntax.json"></a>

```
{
  "[CertificateValidity](#cfn-pcaconnectorad-template-templatev2-certificatevalidity)" : CertificateValidity,
  "[EnrollmentFlags](#cfn-pcaconnectorad-template-templatev2-enrollmentflags)" : EnrollmentFlagsV2,
  "[Extensions](#cfn-pcaconnectorad-template-templatev2-extensions)" : ExtensionsV2,
  "[GeneralFlags](#cfn-pcaconnectorad-template-templatev2-generalflags)" : GeneralFlagsV2,
  "[PrivateKeyAttributes](#cfn-pcaconnectorad-template-templatev2-privatekeyattributes)" : PrivateKeyAttributesV2,
  "[PrivateKeyFlags](#cfn-pcaconnectorad-template-templatev2-privatekeyflags)" : PrivateKeyFlagsV2,
  "[SubjectNameFlags](#cfn-pcaconnectorad-template-templatev2-subjectnameflags)" : SubjectNameFlagsV2,
  "[SupersededTemplates](#cfn-pcaconnectorad-template-templatev2-supersededtemplates)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-templatev2-syntax.yaml"></a>

```
  [CertificateValidity](#cfn-pcaconnectorad-template-templatev2-certificatevalidity): 
    CertificateValidity
  [EnrollmentFlags](#cfn-pcaconnectorad-template-templatev2-enrollmentflags): 
    EnrollmentFlagsV2
  [Extensions](#cfn-pcaconnectorad-template-templatev2-extensions): 
    ExtensionsV2
  [GeneralFlags](#cfn-pcaconnectorad-template-templatev2-generalflags): 
    GeneralFlagsV2
  [PrivateKeyAttributes](#cfn-pcaconnectorad-template-templatev2-privatekeyattributes): 
    PrivateKeyAttributesV2
  [PrivateKeyFlags](#cfn-pcaconnectorad-template-templatev2-privatekeyflags): 
    PrivateKeyFlagsV2
  [SubjectNameFlags](#cfn-pcaconnectorad-template-templatev2-subjectnameflags): 
    SubjectNameFlagsV2
  [SupersededTemplates](#cfn-pcaconnectorad-template-templatev2-supersededtemplates): 
    - String
```

## Properties<a name="aws-properties-pcaconnectorad-template-templatev2-properties"></a>

`CertificateValidity`  <a name="cfn-pcaconnectorad-template-templatev2-certificatevalidity"></a>
Certificate validity describes the validity and renewal periods of a certificate\.  
*Required*: Yes  
*Type*: [CertificateValidity](aws-properties-pcaconnectorad-template-certificatevalidity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnrollmentFlags`  <a name="cfn-pcaconnectorad-template-templatev2-enrollmentflags"></a>
Enrollment flags describe the enrollment settings for certificates such as using the existing private key and deleting expired or revoked certificates\.  
*Required*: Yes  
*Type*: [EnrollmentFlagsV2](aws-properties-pcaconnectorad-template-enrollmentflagsv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Extensions`  <a name="cfn-pcaconnectorad-template-templatev2-extensions"></a>
Extensions describe the key usage extensions and application policies for a template\.  
*Required*: Yes  
*Type*: [ExtensionsV2](aws-properties-pcaconnectorad-template-extensionsv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeneralFlags`  <a name="cfn-pcaconnectorad-template-templatev2-generalflags"></a>
General flags describe whether the template is used for computers or users and if the template can be used with autoenrollment\.  
*Required*: Yes  
*Type*: [GeneralFlagsV2](aws-properties-pcaconnectorad-template-generalflagsv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKeyAttributes`  <a name="cfn-pcaconnectorad-template-templatev2-privatekeyattributes"></a>
Private key attributes allow you to specify the minimal key length, key spec, and cryptographic providers for the private key of a certificate for v2 templates\. V2 templates allow you to use Legacy Cryptographic Service Providers\.  
*Required*: Yes  
*Type*: [PrivateKeyAttributesV2](aws-properties-pcaconnectorad-template-privatekeyattributesv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKeyFlags`  <a name="cfn-pcaconnectorad-template-templatev2-privatekeyflags"></a>
Private key flags for v2 templates specify the client compatibility, if the private key can be exported, and if user input is required when using a private key\.   
*Required*: Yes  
*Type*: [PrivateKeyFlagsV2](aws-properties-pcaconnectorad-template-privatekeyflagsv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubjectNameFlags`  <a name="cfn-pcaconnectorad-template-templatev2-subjectnameflags"></a>
Subject name flags describe the subject name and subject alternate name that is included in a certificate\.  
*Required*: Yes  
*Type*: [SubjectNameFlagsV2](aws-properties-pcaconnectorad-template-subjectnameflagsv2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupersededTemplates`  <a name="cfn-pcaconnectorad-template-templatev2-supersededtemplates"></a>
List of templates in Active Directory that are superseded by this template\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)