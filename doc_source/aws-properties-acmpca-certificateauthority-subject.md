# AWS::ACMPCA::CertificateAuthority Subject<a name="aws-properties-acmpca-certificateauthority-subject"></a>

ASN1 subject for the certificate authority\.

## Syntax<a name="aws-properties-acmpca-certificateauthority-subject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificateauthority-subject-syntax.json"></a>

```
{
  "[CommonName](#cfn-acmpca-certificateauthority-subject-commonname)" : String,
  "[Country](#cfn-acmpca-certificateauthority-subject-country)" : String,
  "[DistinguishedNameQualifier](#cfn-acmpca-certificateauthority-subject-distinguishednamequalifier)" : String,
  "[GenerationQualifier](#cfn-acmpca-certificateauthority-subject-generationqualifier)" : String,
  "[GivenName](#cfn-acmpca-certificateauthority-subject-givenname)" : String,
  "[Initials](#cfn-acmpca-certificateauthority-subject-initials)" : String,
  "[Locality](#cfn-acmpca-certificateauthority-subject-locality)" : String,
  "[Organization](#cfn-acmpca-certificateauthority-subject-organization)" : String,
  "[OrganizationalUnit](#cfn-acmpca-certificateauthority-subject-organizationalunit)" : String,
  "[Pseudonym](#cfn-acmpca-certificateauthority-subject-pseudonym)" : String,
  "[SerialNumber](#cfn-acmpca-certificateauthority-subject-serialnumber)" : String,
  "[State](#cfn-acmpca-certificateauthority-subject-state)" : String,
  "[Surname](#cfn-acmpca-certificateauthority-subject-surname)" : String,
  "[Title](#cfn-acmpca-certificateauthority-subject-title)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificateauthority-subject-syntax.yaml"></a>

```
  [CommonName](#cfn-acmpca-certificateauthority-subject-commonname): String
  [Country](#cfn-acmpca-certificateauthority-subject-country): String
  [DistinguishedNameQualifier](#cfn-acmpca-certificateauthority-subject-distinguishednamequalifier): String
  [GenerationQualifier](#cfn-acmpca-certificateauthority-subject-generationqualifier): String
  [GivenName](#cfn-acmpca-certificateauthority-subject-givenname): String
  [Initials](#cfn-acmpca-certificateauthority-subject-initials): String
  [Locality](#cfn-acmpca-certificateauthority-subject-locality): String
  [Organization](#cfn-acmpca-certificateauthority-subject-organization): String
  [OrganizationalUnit](#cfn-acmpca-certificateauthority-subject-organizationalunit): String
  [Pseudonym](#cfn-acmpca-certificateauthority-subject-pseudonym): String
  [SerialNumber](#cfn-acmpca-certificateauthority-subject-serialnumber): String
  [State](#cfn-acmpca-certificateauthority-subject-state): String
  [Surname](#cfn-acmpca-certificateauthority-subject-surname): String
  [Title](#cfn-acmpca-certificateauthority-subject-title): String
```

## Properties<a name="aws-properties-acmpca-certificateauthority-subject-properties"></a>

`CommonName`  <a name="cfn-acmpca-certificateauthority-subject-commonname"></a>
Fully qualified domain name \(FQDN\) associated with the certificate subject\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Country`  <a name="cfn-acmpca-certificateauthority-subject-country"></a>
Two\-digit code that specifies the country in which the certificate subject located\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DistinguishedNameQualifier`  <a name="cfn-acmpca-certificateauthority-subject-distinguishednamequalifier"></a>
Disambiguating information for the certificate subject\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GenerationQualifier`  <a name="cfn-acmpca-certificateauthority-subject-generationqualifier"></a>
Typically a qualifier appended to the name of an individual\. Examples include Jr\. for junior, Sr\. for senior, and III for third\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GivenName`  <a name="cfn-acmpca-certificateauthority-subject-givenname"></a>
First name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Initials`  <a name="cfn-acmpca-certificateauthority-subject-initials"></a>
 Concatenation that typically contains the first letter of the GivenName, the first letter of the middle name if one exists, and the first letter of the SurName\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Locality`  <a name="cfn-acmpca-certificateauthority-subject-locality"></a>
The locality \(such as a city or town\) in which the certificate subject is located\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Organization`  <a name="cfn-acmpca-certificateauthority-subject-organization"></a>
Legal name of the organization with which the certificate subject is affiliated\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrganizationalUnit`  <a name="cfn-acmpca-certificateauthority-subject-organizationalunit"></a>
A subdivision or unit of the organization \(such as sales or finance\) with which the certificate subject is affiliated\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Pseudonym`  <a name="cfn-acmpca-certificateauthority-subject-pseudonym"></a>
Typically a shortened version of a longer GivenName\. For example, Jonathan is often shortened to John\. Elizabeth is often shortened to Beth, Liz, or Eliza\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SerialNumber`  <a name="cfn-acmpca-certificateauthority-subject-serialnumber"></a>
The certificate serial number\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`State`  <a name="cfn-acmpca-certificateauthority-subject-state"></a>
State in which the subject of the certificate is located\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Surname`  <a name="cfn-acmpca-certificateauthority-subject-surname"></a>
Family name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Title`  <a name="cfn-acmpca-certificateauthority-subject-title"></a>
A personal title such as Mr\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)