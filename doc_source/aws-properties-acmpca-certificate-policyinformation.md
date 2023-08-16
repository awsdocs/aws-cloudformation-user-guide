# AWS::ACMPCA::Certificate PolicyInformation<a name="aws-properties-acmpca-certificate-policyinformation"></a>

Defines the X\.509 `CertificatePolicies` extension\.

## Syntax<a name="aws-properties-acmpca-certificate-policyinformation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-policyinformation-syntax.json"></a>

```
{
  "[CertPolicyId](#cfn-acmpca-certificate-policyinformation-certpolicyid)" : String,
  "[PolicyQualifiers](#cfn-acmpca-certificate-policyinformation-policyqualifiers)" : [ PolicyQualifierInfo, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificate-policyinformation-syntax.yaml"></a>

```
  [CertPolicyId](#cfn-acmpca-certificate-policyinformation-certpolicyid): String
  [PolicyQualifiers](#cfn-acmpca-certificate-policyinformation-policyqualifiers): 
    - PolicyQualifierInfo
```

## Properties<a name="aws-properties-acmpca-certificate-policyinformation-properties"></a>

`CertPolicyId`  <a name="cfn-acmpca-certificate-policyinformation-certpolicyid"></a>
Specifies the object identifier \(OID\) of the certificate policy under which the certificate was issued\. For more information, see NIST's definition of [Object Identifier \(OID\)](https://csrc.nist.gov/glossary/term/Object_Identifier)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Pattern*: `^([0-2])\.([0-9]|([0-3][0-9]))((\.([0-9]+)){0,126})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyQualifiers`  <a name="cfn-acmpca-certificate-policyinformation-policyqualifiers"></a>
Modifies the given `CertPolicyId` with a qualifier\. AWS Private CA supports the certification practice statement \(CPS\) qualifier\.  
*Required*: No  
*Type*: List of [PolicyQualifierInfo](aws-properties-acmpca-certificate-policyqualifierinfo.md)  
*Maximum*: `20`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)