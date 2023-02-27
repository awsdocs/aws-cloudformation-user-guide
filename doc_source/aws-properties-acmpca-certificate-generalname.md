# AWS::ACMPCA::Certificate GeneralName<a name="aws-properties-acmpca-certificate-generalname"></a>

Describes an ASN\.1 X\.400 `GeneralName` as defined in [RFC 5280](https://datatracker.ietf.org/doc/html/rfc5280)\. Only one of the following naming options should be provided\. Providing more than one option results in an `InvalidArgsException` error\.

## Syntax<a name="aws-properties-acmpca-certificate-generalname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-generalname-syntax.json"></a>

```
{
  "[DirectoryName](#cfn-acmpca-certificate-generalname-directoryname)" : Subject,
  "[DnsName](#cfn-acmpca-certificate-generalname-dnsname)" : String,
  "[EdiPartyName](#cfn-acmpca-certificate-generalname-edipartyname)" : EdiPartyName,
  "[IpAddress](#cfn-acmpca-certificate-generalname-ipaddress)" : String,
  "[OtherName](#cfn-acmpca-certificate-generalname-othername)" : OtherName,
  "[RegisteredId](#cfn-acmpca-certificate-generalname-registeredid)" : String,
  "[Rfc822Name](#cfn-acmpca-certificate-generalname-rfc822name)" : String,
  "[UniformResourceIdentifier](#cfn-acmpca-certificate-generalname-uniformresourceidentifier)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificate-generalname-syntax.yaml"></a>

```
  [DirectoryName](#cfn-acmpca-certificate-generalname-directoryname): 
    Subject
  [DnsName](#cfn-acmpca-certificate-generalname-dnsname): String
  [EdiPartyName](#cfn-acmpca-certificate-generalname-edipartyname): 
    EdiPartyName
  [IpAddress](#cfn-acmpca-certificate-generalname-ipaddress): String
  [OtherName](#cfn-acmpca-certificate-generalname-othername): 
    OtherName
  [RegisteredId](#cfn-acmpca-certificate-generalname-registeredid): String
  [Rfc822Name](#cfn-acmpca-certificate-generalname-rfc822name): String
  [UniformResourceIdentifier](#cfn-acmpca-certificate-generalname-uniformresourceidentifier): String
```

## Properties<a name="aws-properties-acmpca-certificate-generalname-properties"></a>

`DirectoryName`  <a name="cfn-acmpca-certificate-generalname-directoryname"></a>
Contains information about the certificate subject\. The certificate can be one issued by your private certificate authority \(CA\) or it can be your private CA certificate\. The Subject field in the certificate identifies the entity that owns or controls the public key in the certificate\. The entity can be a user, computer, device, or service\. The Subject must contain an X\.500 distinguished name \(DN\)\. A DN is a sequence of relative distinguished names \(RDNs\)\. The RDNs are separated by commas in the certificate\. The DN must be unique for each entity, but your private CA can issue more than one certificate with the same DN to the same entity\.  
*Required*: No  
*Type*: [Subject](aws-properties-acmpca-certificate-subject.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DnsName`  <a name="cfn-acmpca-certificate-generalname-dnsname"></a>
Represents `GeneralName` as a DNS name\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `253`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EdiPartyName`  <a name="cfn-acmpca-certificate-generalname-edipartyname"></a>
Represents `GeneralName` as an `EdiPartyName` object\.  
*Required*: No  
*Type*: [EdiPartyName](aws-properties-acmpca-certificate-edipartyname.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpAddress`  <a name="cfn-acmpca-certificate-generalname-ipaddress"></a>
Represents `GeneralName` as an IPv4 or IPv6 address\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `39`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OtherName`  <a name="cfn-acmpca-certificate-generalname-othername"></a>
Represents `GeneralName` using an `OtherName` object\.  
*Required*: No  
*Type*: [OtherName](aws-properties-acmpca-certificate-othername.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RegisteredId`  <a name="cfn-acmpca-certificate-generalname-registeredid"></a>
 Represents `GeneralName` as an object identifier \(OID\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Pattern*: `^([0-2])\.([0-9]|([0-3][0-9]))((\.([0-9]+)){0,126})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rfc822Name`  <a name="cfn-acmpca-certificate-generalname-rfc822name"></a>
Represents `GeneralName` as an [RFC 822](https://datatracker.ietf.org/doc/html/rfc822) email address\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UniformResourceIdentifier`  <a name="cfn-acmpca-certificate-generalname-uniformresourceidentifier"></a>
Represents `GeneralName` as a URI\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `253`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)