# AWS::ACMPCA::Certificate Subject<a name="aws-properties-acmpca-certificate-subject"></a>

Contains information about the certificate subject\. The `Subject` field in the certificate identifies the entity that owns or controls the public key in the certificate\. The entity can be a user, computer, device, or service\. The `Subject `must contain an X\.500 distinguished name \(DN\)\. A DN is a sequence of relative distinguished names \(RDNs\)\. The RDNs are separated by commas in the certificate\.

## Syntax<a name="aws-properties-acmpca-certificate-subject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-subject-syntax.json"></a>

```
{
  "[CommonName](#cfn-acmpca-certificate-subject-commonname)" : String,
  "[Country](#cfn-acmpca-certificate-subject-country)" : String,
  "[CustomAttributes](#cfn-acmpca-certificate-subject-customattributes)" : [ CustomAttribute, ... ],
  "[DistinguishedNameQualifier](#cfn-acmpca-certificate-subject-distinguishednamequalifier)" : String,
  "[GenerationQualifier](#cfn-acmpca-certificate-subject-generationqualifier)" : String,
  "[GivenName](#cfn-acmpca-certificate-subject-givenname)" : String,
  "[Initials](#cfn-acmpca-certificate-subject-initials)" : String,
  "[Locality](#cfn-acmpca-certificate-subject-locality)" : String,
  "[Organization](#cfn-acmpca-certificate-subject-organization)" : String,
  "[OrganizationalUnit](#cfn-acmpca-certificate-subject-organizationalunit)" : String,
  "[Pseudonym](#cfn-acmpca-certificate-subject-pseudonym)" : String,
  "[SerialNumber](#cfn-acmpca-certificate-subject-serialnumber)" : String,
  "[State](#cfn-acmpca-certificate-subject-state)" : String,
  "[Surname](#cfn-acmpca-certificate-subject-surname)" : String,
  "[Title](#cfn-acmpca-certificate-subject-title)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificate-subject-syntax.yaml"></a>

```
  [CommonName](#cfn-acmpca-certificate-subject-commonname): String
  [Country](#cfn-acmpca-certificate-subject-country): String
  [CustomAttributes](#cfn-acmpca-certificate-subject-customattributes): 
    - CustomAttribute
  [DistinguishedNameQualifier](#cfn-acmpca-certificate-subject-distinguishednamequalifier): String
  [GenerationQualifier](#cfn-acmpca-certificate-subject-generationqualifier): String
  [GivenName](#cfn-acmpca-certificate-subject-givenname): String
  [Initials](#cfn-acmpca-certificate-subject-initials): String
  [Locality](#cfn-acmpca-certificate-subject-locality): String
  [Organization](#cfn-acmpca-certificate-subject-organization): String
  [OrganizationalUnit](#cfn-acmpca-certificate-subject-organizationalunit): String
  [Pseudonym](#cfn-acmpca-certificate-subject-pseudonym): String
  [SerialNumber](#cfn-acmpca-certificate-subject-serialnumber): String
  [State](#cfn-acmpca-certificate-subject-state): String
  [Surname](#cfn-acmpca-certificate-subject-surname): String
  [Title](#cfn-acmpca-certificate-subject-title): String
```

## Properties<a name="aws-properties-acmpca-certificate-subject-properties"></a>

`CommonName`  <a name="cfn-acmpca-certificate-subject-commonname"></a>
For CA and end\-entity certificates in a private PKI, the common name \(CN\) can be any string within the length limit\.  
Note: In publicly trusted certificates, the common name must be a fully qualified domain name \(FQDN\) associated with the certificate subject\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Country`  <a name="cfn-acmpca-certificate-subject-country"></a>
Two\-digit code that specifies the country in which the certificate subject located\.  
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `2`  
*Pattern*: `[A-Za-z]{2}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CustomAttributes`  <a name="cfn-acmpca-certificate-subject-customattributes"></a>
  
Contains a sequence of one or more X\.500 relative distinguished names \(RDNs\), each of which consists of an object identifier \(OID\) and a value\. For more information, see NIST’s definition of [Object Identifier \(OID\)](https://csrc.nist.gov/glossary/term/Object_Identifier)\.  
Custom attributes cannot be used in combination with standard attributes\.
*Required*: No  
*Type*: List of [CustomAttribute](aws-properties-acmpca-certificate-customattribute.md)  
*Maximum*: `30`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DistinguishedNameQualifier`  <a name="cfn-acmpca-certificate-subject-distinguishednamequalifier"></a>
Disambiguating information for the certificate subject\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Pattern*: `[a-zA-Z0-9'()+-.?:/= ]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GenerationQualifier`  <a name="cfn-acmpca-certificate-subject-generationqualifier"></a>
Typically a qualifier appended to the name of an individual\. Examples include Jr\. for junior, Sr\. for senior, and III for third\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GivenName`  <a name="cfn-acmpca-certificate-subject-givenname"></a>
First name\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `16`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Initials`  <a name="cfn-acmpca-certificate-subject-initials"></a>
Concatenation that typically contains the first letter of the **GivenName**, the first letter of the middle name if one exists, and the first letter of the **Surname**\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Locality`  <a name="cfn-acmpca-certificate-subject-locality"></a>
The locality \(such as a city or town\) in which the certificate subject is located\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Organization`  <a name="cfn-acmpca-certificate-subject-organization"></a>
Legal name of the organization with which the certificate subject is affiliated\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrganizationalUnit`  <a name="cfn-acmpca-certificate-subject-organizationalunit"></a>
A subdivision or unit of the organization \(such as sales or finance\) with which the certificate subject is affiliated\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Pseudonym`  <a name="cfn-acmpca-certificate-subject-pseudonym"></a>
Typically a shortened version of a longer **GivenName**\. For example, Jonathan is often shortened to John\. Elizabeth is often shortened to Beth, Liz, or Eliza\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SerialNumber`  <a name="cfn-acmpca-certificate-subject-serialnumber"></a>
The certificate serial number\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Pattern*: `[a-zA-Z0-9'()+-.?:/= ]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`State`  <a name="cfn-acmpca-certificate-subject-state"></a>
State in which the subject of the certificate is located\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Surname`  <a name="cfn-acmpca-certificate-subject-surname"></a>
Family name\. In the US and the UK, for example, the surname of an individual is ordered last\. In Asian cultures the surname is typically ordered first\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `40`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Title`  <a name="cfn-acmpca-certificate-subject-title"></a>
A title such as Mr\. or Ms\., which is pre\-pended to the name to refer formally to the certificate subject\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)