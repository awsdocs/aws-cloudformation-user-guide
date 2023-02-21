# AWS::ACMPCA::Certificate EdiPartyName<a name="aws-properties-acmpca-certificate-edipartyname"></a>

Describes an Electronic Data Interchange \(EDI\) entity as described in as defined in [Subject Alternative Name](https://datatracker.ietf.org/doc/html/rfc5280) in RFC 5280\.

## Syntax<a name="aws-properties-acmpca-certificate-edipartyname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-edipartyname-syntax.json"></a>

```
{
  "[NameAssigner](#cfn-acmpca-certificate-edipartyname-nameassigner)" : String,
  "[PartyName](#cfn-acmpca-certificate-edipartyname-partyname)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificate-edipartyname-syntax.yaml"></a>

```
  [NameAssigner](#cfn-acmpca-certificate-edipartyname-nameassigner): String
  [PartyName](#cfn-acmpca-certificate-edipartyname-partyname): String
```

## Properties<a name="aws-properties-acmpca-certificate-edipartyname-properties"></a>

`NameAssigner`  <a name="cfn-acmpca-certificate-edipartyname-nameassigner"></a>
Specifies the name assigner\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PartyName`  <a name="cfn-acmpca-certificate-edipartyname-partyname"></a>
Specifies the party name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)