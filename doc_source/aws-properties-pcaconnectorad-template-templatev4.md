# AWS::PCAConnectorAD::Template TemplateV4<a name="aws-properties-pcaconnectorad-template-templatev4"></a>

v4 template schema that can use either Legacy Cryptographic Providers or Key Storage Providers\.

## Syntax<a name="aws-properties-pcaconnectorad-template-templatev4-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-templatev4-syntax.json"></a>

```
{
  "[CertificateValidity](#cfn-pcaconnectorad-template-templatev4-certificatevalidity)" : CertificateValidity,
  "[EnrollmentFlags](#cfn-pcaconnectorad-template-templatev4-enrollmentflags)" : EnrollmentFlagsV4,
  "[Extensions](#cfn-pcaconnectorad-template-templatev4-extensions)" : ExtensionsV4,
  "[GeneralFlags](#cfn-pcaconnectorad-template-templatev4-generalflags)" : GeneralFlagsV4,
  "[HashAlgorithm](#cfn-pcaconnectorad-template-templatev4-hashalgorithm)" : String,
  "[PrivateKeyAttributes](#cfn-pcaconnectorad-template-templatev4-privatekeyattributes)" : PrivateKeyAttributesV4,
  "[PrivateKeyFlags](#cfn-pcaconnectorad-template-templatev4-privatekeyflags)" : PrivateKeyFlagsV4,
  "[SubjectNameFlags](#cfn-pcaconnectorad-template-templatev4-subjectnameflags)" : SubjectNameFlagsV4,
  "[SupersededTemplates](#cfn-pcaconnectorad-template-templatev4-supersededtemplates)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-templatev4-syntax.yaml"></a>

```
  [CertificateValidity](#cfn-pcaconnectorad-template-templatev4-certificatevalidity): 
    CertificateValidity
  [EnrollmentFlags](#cfn-pcaconnectorad-template-templatev4-enrollmentflags): 
    EnrollmentFlagsV4
  [Extensions](#cfn-pcaconnectorad-template-templatev4-extensions): 
    ExtensionsV4
  [GeneralFlags](#cfn-pcaconnectorad-template-templatev4-generalflags): 
    GeneralFlagsV4
  [HashAlgorithm](#cfn-pcaconnectorad-template-templatev4-hashalgorithm): String
  [PrivateKeyAttributes](#cfn-pcaconnectorad-template-templatev4-privatekeyattributes): 
    PrivateKeyAttributesV4
  [PrivateKeyFlags](#cfn-pcaconnectorad-template-templatev4-privatekeyflags): 
    PrivateKeyFlagsV4
  [SubjectNameFlags](#cfn-pcaconnectorad-template-templatev4-subjectnameflags): 
    SubjectNameFlagsV4
  [SupersededTemplates](#cfn-pcaconnectorad-template-templatev4-supersededtemplates): 
    - String
```

## Properties<a name="aws-properties-pcaconnectorad-template-templatev4-properties"></a>

`CertificateValidity`  <a name="cfn-pcaconnectorad-template-templatev4-certificatevalidity"></a>
Certificate validity describes the validity and renewal periods of a certificate\.  
*Required*: Yes  
*Type*: [CertificateValidity](aws-properties-pcaconnectorad-template-certificatevalidity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnrollmentFlags`  <a name="cfn-pcaconnectorad-template-templatev4-enrollmentflags"></a>
Enrollment flags describe the enrollment settings for certificates using the existing private key and deleting expired or revoked certificates\.  
*Required*: Yes  
*Type*: [EnrollmentFlagsV4](aws-properties-pcaconnectorad-template-enrollmentflagsv4.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Extensions`  <a name="cfn-pcaconnectorad-template-templatev4-extensions"></a>
Extensions describe the key usage extensions and application policies for a template\.  
*Required*: Yes  
*Type*: [ExtensionsV4](aws-properties-pcaconnectorad-template-extensionsv4.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeneralFlags`  <a name="cfn-pcaconnectorad-template-templatev4-generalflags"></a>
General flags describe whether the template is used for computers or users and if the template can be used with autoenrollment\.  
*Required*: Yes  
*Type*: [GeneralFlagsV4](aws-properties-pcaconnectorad-template-generalflagsv4.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HashAlgorithm`  <a name="cfn-pcaconnectorad-template-templatev4-hashalgorithm"></a>
Specifies the hash algorithm used to hash the private key\. Hash algorithm can only be specified when using Key Storage Providers\.  
*Required*: No  
*Type*: String  
*Allowed values*: `SHA256 | SHA384 | SHA512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKeyAttributes`  <a name="cfn-pcaconnectorad-template-templatev4-privatekeyattributes"></a>
Private key attributes allow you to specify the minimal key length, key spec, key usage, and cryptographic providers for the private key of a certificate for v4 templates\. V4 templates allow you to use either Key Storage Providers or Legacy Cryptographic Service Providers\. You specify the cryptography provider category in private key flags\.  
*Required*: Yes  
*Type*: [PrivateKeyAttributesV4](aws-properties-pcaconnectorad-template-privatekeyattributesv4.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKeyFlags`  <a name="cfn-pcaconnectorad-template-templatev4-privatekeyflags"></a>
Private key flags for v4 templates specify the client compatibility, if the private key can be exported, if user input is required when using a private key, if an alternate signature algorithm should be used, and if certificates are renewed using the same private key\.  
*Required*: Yes  
*Type*: [PrivateKeyFlagsV4](aws-properties-pcaconnectorad-template-privatekeyflagsv4.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubjectNameFlags`  <a name="cfn-pcaconnectorad-template-templatev4-subjectnameflags"></a>
Subject name flags describe the subject name and subject alternate name that is included in a certificate\.  
*Required*: Yes  
*Type*: [SubjectNameFlagsV4](aws-properties-pcaconnectorad-template-subjectnameflagsv4.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupersededTemplates`  <a name="cfn-pcaconnectorad-template-templatev4-supersededtemplates"></a>
List of templates in Active Directory that are superseded by this template\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)