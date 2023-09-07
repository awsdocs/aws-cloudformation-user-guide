# AWS::PCAConnectorAD::Template TemplateV3<a name="aws-properties-pcaconnectorad-template-templatev3"></a>

v3 template schema that uses Key Storage Providers\.

## Syntax<a name="aws-properties-pcaconnectorad-template-templatev3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-templatev3-syntax.json"></a>

```
{
  "[CertificateValidity](#cfn-pcaconnectorad-template-templatev3-certificatevalidity)" : CertificateValidity,
  "[EnrollmentFlags](#cfn-pcaconnectorad-template-templatev3-enrollmentflags)" : EnrollmentFlagsV3,
  "[Extensions](#cfn-pcaconnectorad-template-templatev3-extensions)" : ExtensionsV3,
  "[GeneralFlags](#cfn-pcaconnectorad-template-templatev3-generalflags)" : GeneralFlagsV3,
  "[HashAlgorithm](#cfn-pcaconnectorad-template-templatev3-hashalgorithm)" : String,
  "[PrivateKeyAttributes](#cfn-pcaconnectorad-template-templatev3-privatekeyattributes)" : PrivateKeyAttributesV3,
  "[PrivateKeyFlags](#cfn-pcaconnectorad-template-templatev3-privatekeyflags)" : PrivateKeyFlagsV3,
  "[SubjectNameFlags](#cfn-pcaconnectorad-template-templatev3-subjectnameflags)" : SubjectNameFlagsV3,
  "[SupersededTemplates](#cfn-pcaconnectorad-template-templatev3-supersededtemplates)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-templatev3-syntax.yaml"></a>

```
  [CertificateValidity](#cfn-pcaconnectorad-template-templatev3-certificatevalidity): 
    CertificateValidity
  [EnrollmentFlags](#cfn-pcaconnectorad-template-templatev3-enrollmentflags): 
    EnrollmentFlagsV3
  [Extensions](#cfn-pcaconnectorad-template-templatev3-extensions): 
    ExtensionsV3
  [GeneralFlags](#cfn-pcaconnectorad-template-templatev3-generalflags): 
    GeneralFlagsV3
  [HashAlgorithm](#cfn-pcaconnectorad-template-templatev3-hashalgorithm): String
  [PrivateKeyAttributes](#cfn-pcaconnectorad-template-templatev3-privatekeyattributes): 
    PrivateKeyAttributesV3
  [PrivateKeyFlags](#cfn-pcaconnectorad-template-templatev3-privatekeyflags): 
    PrivateKeyFlagsV3
  [SubjectNameFlags](#cfn-pcaconnectorad-template-templatev3-subjectnameflags): 
    SubjectNameFlagsV3
  [SupersededTemplates](#cfn-pcaconnectorad-template-templatev3-supersededtemplates): 
    - String
```

## Properties<a name="aws-properties-pcaconnectorad-template-templatev3-properties"></a>

`CertificateValidity`  <a name="cfn-pcaconnectorad-template-templatev3-certificatevalidity"></a>
Certificate validity describes the validity and renewal periods of a certificate\.  
*Required*: Yes  
*Type*: [CertificateValidity](aws-properties-pcaconnectorad-template-certificatevalidity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnrollmentFlags`  <a name="cfn-pcaconnectorad-template-templatev3-enrollmentflags"></a>
Enrollment flags describe the enrollment settings for certificates such as using the existing private key and deleting expired or revoked certificates\.  
*Required*: Yes  
*Type*: [EnrollmentFlagsV3](aws-properties-pcaconnectorad-template-enrollmentflagsv3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Extensions`  <a name="cfn-pcaconnectorad-template-templatev3-extensions"></a>
Extensions describe the key usage extensions and application policies for a template\.  
*Required*: Yes  
*Type*: [ExtensionsV3](aws-properties-pcaconnectorad-template-extensionsv3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeneralFlags`  <a name="cfn-pcaconnectorad-template-templatev3-generalflags"></a>
General flags describe whether the template is used for computers or users and if the template can be used with autoenrollment\.  
*Required*: Yes  
*Type*: [GeneralFlagsV3](aws-properties-pcaconnectorad-template-generalflagsv3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HashAlgorithm`  <a name="cfn-pcaconnectorad-template-templatev3-hashalgorithm"></a>
Specifies the hash algorithm used to hash the private key\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SHA256 | SHA384 | SHA512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKeyAttributes`  <a name="cfn-pcaconnectorad-template-templatev3-privatekeyattributes"></a>
Private key attributes allow you to specify the algorithm, minimal key length, key spec, key usage, and cryptographic providers for the private key of a certificate for v3 templates\. V3 templates allow you to use Key Storage Providers\.  
*Required*: Yes  
*Type*: [PrivateKeyAttributesV3](aws-properties-pcaconnectorad-template-privatekeyattributesv3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKeyFlags`  <a name="cfn-pcaconnectorad-template-templatev3-privatekeyflags"></a>
Private key flags for v3 templates specify the client compatibility, if the private key can be exported, if user input is required when using a private key, and if an alternate signature algorithm should be used\.  
*Required*: Yes  
*Type*: [PrivateKeyFlagsV3](aws-properties-pcaconnectorad-template-privatekeyflagsv3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubjectNameFlags`  <a name="cfn-pcaconnectorad-template-templatev3-subjectnameflags"></a>
Subject name flags describe the subject name and subject alternate name that is included in a certificate\.  
*Required*: Yes  
*Type*: [SubjectNameFlagsV3](aws-properties-pcaconnectorad-template-subjectnameflagsv3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupersededTemplates`  <a name="cfn-pcaconnectorad-template-templatev3-supersededtemplates"></a>
List of templates in Active Directory that are superseded by this template\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)